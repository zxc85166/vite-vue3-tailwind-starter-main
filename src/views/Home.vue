<script setup>
import { useI18n } from 'vue-i18n'
import {
  Disclosure,
  DisclosureButton,
  DisclosurePanel,
} from '@headlessui/vue'
const { t } = useI18n();
</script>

<template>
  <div class="bg-gray-200">
    <div
      class="max-w-screen-xl bg-white border border-gray-300 px-4 py-12 mx-auto sm:px-6 lg:py-16 lg:px-8 grid grid-flow-row auto-rows-max gap-y-6"
    >
      <!-- 團體照 -->
      <div
        class="card flex-initial shadow-sm bg-accent text-accent-content text-center mx-auto w-full md:w-4/5"
      >
        <figure>
          <img src="@/assets/images/home.jpg" />
        </figure>
        <div class="card-body bg-green-100">
          <h2 class="card-title">Weeekly 4th Mini Album</h2>
          <p>Play Game : Holiday</p>
        </div>
      </div>
      <!-- 目錄與簡介 -->
      <div class="grid grid-cols-1 md:grid-cols-2 place-content-between gap-y-3">
        <!-- 目錄 -->
        <div class="border border-gray-300 p-4 max-w-max h-fit order-last md:order-1">
          <span class="font-semibold text-xl">{{ t('home.Directory.directory') }}</span>
          <div class="pt-3 flex flex-col">
            <span>
              <a href="#s-1">1</a>
              . {{ t('home.Directory.summary') }}
            </span>
            <span>
              <a href="#s-2">2</a>
              . {{ t('home.Directory.member') }}
            </span>
            <span class="pl-6">
              <a href="#s-2.1">2.1</a>
              . {{ t('home.Directory.CP') }}
            </span>
            <span>
              <a href="#s-3">3</a>
              . {{ t('home.Directory.appearance') }}
            </span>
            <span>
              <a href="#s-4">4</a>
              . {{ t('home.Directory.world View') }}
            </span>
            <span>
              <a href="#s-5">5</a>
              . {{ t('home.Directory.album List') }}
            </span>
            <span>
              <a href="#s-6">6</a>
              . {{ t('home.Directory.MV') }}
            </span>
            <span>
              <a href="#s-7">7</a>
              . {{ t('home.Directory.activity') }}
            </span>
            <span class="pl-6">
              <a href="#s-7.1">7.1</a>
              . V LIVE
            </span>
            <span class="pl-6">
              <a href="#s-7.2">7.2</a>
              . {{ t('home.Directory.advertise') }}
            </span>
            <span class="pl-12">
              <a href="#s-7.2.1">7.2.1</a>
              {{ t('home.Directory.ads') }}
            </span>
            <span>
              <a href="#s-8">8</a>
              . {{ t('home.Directory.award Experience') }}
            </span>
            <span class="pl-6">
              <a href="#s-8.1">8.1</a>
              . {{ t('home.Directory.awards Ceremony') }}
            </span>
            <span>
              <a href="#s-9">9</a>
              . {{ t('home.Directory.fan') }}
            </span>
            <span>
              <a href="#s-10">10</a>
              . {{ t('home.Directory.support') }}
            </span>
            <span>
              <a href="#s-11">11</a>
              . {{ t('home.Directory.chat') }}
            </span>
          </div>
        </div>
        <!-- 簡介 -->
        <div class="grid grid-flow-row border-2 border-blue-100 divide-y leading-9 order-2">
          <!-- logo -->
          <div class="grid grid-cols-3 gap-2 grid-flow-col divide-x m-3">
            <div class="col-span-2 grid place-items-center">
              <img src="@/assets/images/weeekly.png" class="w-3/5" />
            </div>
            <div>
              <div class="mt-3">
                <span class="pl-2 text-xl font-bold text-blue-100">
                  We
                  <span class="text-red-500 ml-[-4px]">e</span>ekly
                </span>
                <p class="pl-2 text-blue-100">{{ t('name.weeekly') }}</p>
              </div>
            </div>
          </div>
          <!-- logo -->
          <!-- 資訊 -->
          <div class="grid grid-cols-3 grid-flow-col grid-flow-row text-center">
            <div
              class="col-span-1 bg-blue-100 text-white font-bold grid place-items-center"
            >{{ t('home.Group Information.debut') }}</div>
            <div class="col-span-2 grid place-items-center">
              <div class="pl-2">
                <p>2020년 6월 30일</p>
                <p>미니 1집 We are</p>
                <p>데뷔일로부터 +491일째</p>
              </div>
            </div>
          </div>
          <div class="grid grid-cols-3 grid-flow-col grid-flow-row">
            <div
              class="col-span-1 bg-blue-100 text-white font-bold grid place-items-center"
            >{{ t('home.Group Information.Music style') }}</div>
            <div class="col-span-2 grid place-items-center">
              <p class="pl-2">댄스, 퓨처 베이스, R&B</p>
            </div>
          </div>
          <div class="grid grid-cols-3 grid-flow-col grid-flow-row">
            <div
              class="col-span-1 bg-blue-100 text-white font-bold grid place-items-center"
            >{{ t('home.Group Information.leader') }}</div>
            <div class="col-span-2 grid place-items-center">
              <span class="pl-2">
                <router-link to="Soojin" class="no-underline hover:underline">{{ t('name.soojin') }}</router-link>
              </span>
            </div>
          </div>
          <div class="grid grid-cols-3 grid-flow-col grid-flow-row">
            <div
              class="col-span-1 bg-blue-100 text-white font-bold grid place-items-center"
            >{{ t('home.Group Information.agency') }}</div>
            <div class="col-span-2 grid place-items-center">
              <img class="w-1/3 m-2" src="@/assets/images/IST.png" />
            </div>
          </div>
          <div class="grid grid-cols-3 grid-flow-col grid-flow-row">
            <div
              class="col-span-1 bg-blue-100 text-white font-bold grid place-items-center"
            >{{ t('home.Group Information.Record company') }}</div>
            <div class="col-span-2 grid place-items-center">
              <img class="w-1/4 m-2" src="@/assets/images/kakao.svg" />
            </div>
          </div>
          <div class="grid grid-cols-3 grid-flow-col grid-flow-row">
            <div
              class="col-span-1 bg-blue-100 text-white font-bold grid place-items-center"
            >{{ t('home.Group Information.fandom') }}</div>
            <div class="col-span-2 grid place-items-center">
              <img class="w-1/4 m-2" src="@/assets/images/Daileee.png" />
            </div>
          </div>
          <div class="grid grid-cols-3 grid-flow-col grid-flow-row">
            <div
              class="col-span-1 bg-blue-100 text-white font-bold grid place-items-center"
            >{{ t('home.Group Information.link') }}</div>
            <div class="col-span-2 flex items-center justify-center gap-[2px] md:gap-3">
              <a href="https://twitter.com/_Weeekly" target="_blank">
                <img class="w-5" src="@/assets/images/twitter.svg" />
              </a>
              <a href="https://www.instagram.com/_weeekly/" target="_blank">
                <img class="w-5" src="@/assets/images/insta.svg" />
              </a>
              <a href="https://www.facebook.com/WeeeklyOfficial" target="_blank">
                <img class="w-5" src="@/assets/images/fb.svg" />
              </a>
              <a href="https://www.youtube.com/channel/UC5rp2rDRSpyKNj-QLytC-tw/" target="_blank">
                <img class="w-5" src="@/assets/images/yt.svg" />
              </a>
              <a href="https://cafe.daum.net/Weeekly" target="_blank">
                <img class="w-5" src="@/assets/images/cafe.png" />
              </a>
              <a href="https://www.weverse.io/weeekly/feed" target="_blank">
                <img class="w-5" src="@/assets/images/weverse.png" />
              </a>
              <a href="https://channels.vlive.tv/A0ABD1" target="_blank">
                <img class="w-5" src="@/assets/images/vlive.svg" />
              </a>
              <a href="https://www.tiktok.com/@weeekly" target="_blank">
                <img class="w-5" src="@/assets/images/tiktok.svg" />
              </a>
            </div>
          </div>
          <!-- 資訊 -->
        </div>
      </div>
      <!-- collapse -->
      <!-- 1. 概要 -->
      <div class="collapse w-full collapse-arrow">
        <input type="checkbox" />
        <div
          class="collapse-title text-xl font-extrabold"
          id="s-1"
        >1. {{ t('home.Directory.summary') }}</div>
        <div class="collapse-content">
          <div class="w-1/2 mx-auto">
            <!-- poster="/skins/senkawa/eff02a509fa92bb835d8902dd4b5b760.gif" -->
            <video src="@/assets/videos/weeekly.mp4" loop autoplay muted playsinline loading="lazy"></video>
          </div>
          <div
            class="border-dashed border-2 border-gray-400 bg-white text-center m-5 p-1 w-1/2 mx-auto"
          >인사드리겠습니다! 本周是Weeekly! 大家好, 我們是Weeekly!</div>
          <div
            class="border-dashed border-2 border-gray-400 bg-white text-center m-5 p-1 w-1/3 mx-auto"
          >Can we do? We can do! Weeekly!</div>

          <div>
            <strong>Weeekly(위클리)</strong>는 플레이엠엔터테인먼트 소속 7인조 걸그룹이며,
            <strong>매일 새롭고 특별한 일주일을 선사한다</strong>는 캐치프레이즈답게 멤버들이 요일을 하나씩 담당하고 있다.
          </div>
        </div>
      </div>
      <!-- 2. 成員 -->
      <div class="collapse w-full collapse-arrow">
        <input type="checkbox" />
        <div
          class="collapse-title text-xl font-extrabold"
          id="s-2"
        >2. {{ t('home.Directory.member') }}</div>
        <div class="collapse-content">
          <div
            class="border-2 border-blue-100 grid grid-cols-2 md:grid-cols-4 bg-white text-center max-w-5xl mx-auto"
          >
            <div class="grid grid-flow-row auto-rows-max border divide-y divide-slate-300">
              <div class="w-full">
                <img class="w-full" src="@/assets/images/soojin.jpg" />
              </div>
              <div
                class="bg-blue-100 text-white font-bold grid place-items-center p-1"
              >{{ t('name.soojin') }}</div>
              <div class="p-1">2001. 12. 12.</div>
              <div class="p-1">
                <p>
                  <strong>{{ t('home.position.leader') }}</strong>
                </p>
                <p>
                  <strong>{{ t('home.position.center') }}</strong>
                </p>
                <p>
                  <strong>{{ t('home.position.main dancer') }}</strong>
                </p>
                {{ t('home.position.sub vocal') }}
              </div>
            </div>
            <div class="grid grid-flow-row auto-rows-max border divide-y divide-slate-300">
              <div class="w-full">
                <img class="w-full" src="@/assets/images/jiyoon.jpg" />
              </div>
              <div
                class="bg-blue-100 text-white font-bold grid place-items-center p-1"
              >{{ t('name.jiyoon') }}</div>
              <div class="p-1">2002. 03. 02.</div>
              <div class="p-1">
                <p>{{ t('home.position.lead vocal') }}</p>
                <p>{{ t('home.position.lead dancer') }}</p>
                <p>{{ t('home.position.rapper') }}</p>
              </div>
            </div>
            <div class="grid grid-flow-row auto-rows-max border divide-y divide-slate-300">
              <div class="w-full">
                <img class="w-full" src="@/assets/images/monday.jpg" />
              </div>
              <div
                class="bg-blue-100 text-white font-bold grid place-items-center p-1"
              >{{ t('name.monday') }}</div>
              <div class="p-1">2002. 05. 10.</div>
              <div class="p-1">
                <p>
                  <strong>{{ t('home.position.main vocal') }}</strong>
                </p>
                <p>
                  <strong>{{ t('home.position.main dancer') }}</strong>
                </p>
                <p>{{ t('home.position.rapper') }}</p>
              </div>
            </div>
            <div class="grid grid-flow-row auto-rows-max border divide-y divide-slate-300">
              <div class="w-full">
                <img class="w-full" src="@/assets/images/soeun.jpg" />
              </div>
              <div
                class="bg-blue-100 text-white font-bold grid place-items-center p-1"
              >{{ t('name.soeun') }}</div>
              <div class="p-1">2002. 10. 26.</div>
              <div class="p-1">
                <p>
                  <strong>{{ t('home.position.main dancer') }}</strong>
                </p>
                {{ t('home.position.lead vocal') }}
              </div>
            </div>
            <div class="grid grid-flow-row auto-rows-max border divide-y divide-slate-300">
              <div class="w-full">
                <img class="w-full" src="@/assets/images/jaehee.jpg" />
              </div>
              <div
                class="bg-blue-100 text-white font-bold grid place-items-center p-1"
              >{{ t('name.jaehee') }}</div>
              <div class="p-1">2004. 03. 18.</div>
              <div class="p-1">
                <p>{{ t('home.position.sub vocal') }}</p>
                {{ t('home.position.rapper') }}
              </div>
            </div>
            <div class="grid grid-flow-row auto-rows-max border divide-y divide-slate-300">
              <div class="w-full">
                <img class="w-full" src="@/assets/images/jihan.jpg" />
              </div>
              <div
                class="bg-blue-100 text-white font-bold grid place-items-center p-1"
              >{{ t('name.jihan') }}</div>
              <div class="p-1">2004. 07. 12.</div>
              <div class="p-1">
                <p>{{ t('home.position.lead vocal') }}</p>
                {{ t('home.position.lead dancer') }}
              </div>
            </div>
            <div class="grid grid-flow-row auto-rows-max border divide-y divide-slate-300">
              <div class="w-full">
                <img class="w-full" src="@/assets/images/zoa.jpg" />
              </div>
              <div
                class="bg-blue-100 text-white font-bold grid place-items-center p-1"
              >{{ t('name.zoa') }}</div>
              <div class="p-1">2005. 05. 31.</div>
              <div class="p-1">
                <p>{{ t('home.position.sub vocal') }}</p>
                {{ t('home.position.rapper') }}
              </div>
            </div>
            <div class="my-auto">
              <div class="w-full">
                <img
                  src="https://w.namu.la/s/1c26fee5598c453828e3ffe98c6c89e06ec73f2d1eb99fe3afecbe29185624233dbf235dc060c371e8a64945b1ad75722d45cf24490330207851085db2de9192ac6690312354d85aa96cbff7fb0c97d81b92a03703999443eda3bb1b2a97b658228c73d8f417ee351f3e422024334317"
                />
              </div>
            </div>
            <div class="col-span-2 md:col-span-4">
              <Disclosure>
                <DisclosureButton class="py-2 font-bold">{{ t('home.DisclosureButton') }}</DisclosureButton>
                <transition
                  enter-active-class="transition duration-100 ease-out"
                  enter-from-class="transform scale-95 opacity-0"
                  enter-to-class="transform scale-100 opacity-100"
                  leave-active-class="transition duration-75 ease-out"
                  leave-from-class="transform scale-100 opacity-100"
                  leave-to-class="transform scale-95 opacity-0"
                >
                  <DisclosurePanel>
                    <div
                      class="grid grid-cols-4 grid-flow-row auto-rows-max divide-y divide-x divide-slate-300 font-bold leading-9"
                    >
                      <div class="bg-blue-100 text-white">이름</div>
                      <div class="bg-blue-100 text-white">이름</div>
                      <div class="bg-blue-100 text-white">이름</div>
                      <div class="bg-blue-100 text-white">이름</div>
                      <div class="text-red-500">{{ t('name.soojin') }}</div>
                      <div>{{ t('week.Monday') }}</div>
                      <div>태양</div>
                      <div>20</div>
                      <div class="text-red-500">{{ t('name.jiyoon') }}</div>
                      <div>{{ t('week.Tuesday') }}</div>
                      <div>태양</div>
                      <div>88</div>
                      <div class="text-red-500">{{ t('name.monday') }}</div>
                      <div>{{ t('week.Wednesday') }}</div>
                      <div>태양</div>
                      <div>76</div>
                      <div class="text-red-500">{{ t('name.soeun') }}</div>
                      <div>{{ t('week.Thursday') }}</div>
                      <div>태양</div>
                      <div>03</div>
                      <div class="text-red-500">{{ t('name.jaehee') }}</div>
                      <div>{{ t('week.Friday') }}</div>
                      <div>태양</div>
                      <div>92</div>
                      <div class="text-red-500">{{ t('name.jihan') }}</div>
                      <div>{{ t('week.Saturday') }}</div>
                      <div>태양</div>
                      <div>96</div>
                      <div class="text-red-500">{{ t('name.zoa') }}</div>
                      <div>{{ t('week.Sunday') }}</div>
                      <div>태양</div>
                      <div>77</div>
                    </div>
                  </DisclosurePanel>
                </transition>
              </Disclosure>
            </div>
          </div>
        </div>
      </div>
      <!-- 2.1. 成員間的CP -->
      <div class="collapse w-full collapse-arrow">
        <input type="checkbox" />
        <div
          class="collapse-title text-xl font-extrabold"
          id="s-2.1"
        >2.1. {{ t('home.Directory.CP') }}</div>
        <div class="collapse-content">
          <div class="mx-5">
            <ul class="list-disc leading-10">
              <li>
                <strong class="text-red-500">페이브걸즈</strong>
                - {{ t('name.soojin') }}, {{ t('name.jiyoon') }}, {{ t('name.jiyoon') }}, {{ t('name.soeun') }}, {{ t('name.jaehee') }}
              </li>
              <li>
                <strong class="text-blue-800">공이(02)즈/ 올라운더즈</strong>
                - {{ t('name.jiyoon') }}, {{ t('name.monday') }}, {{ t('name.soeun') }}
              </li>
              <li>
                <strong class="text-red-500">공사(04)즈/ 공사장</strong>
                - {{ t('name.jaehee') }}, {{ t('name.jihan') }}
              </li>
              <li>
                <strong class="text-blue-800">3월즈</strong>
                - {{ t('name.jiyoon') }}, {{ t('name.jaehee') }}
              </li>
              <li>
                <strong class="text-red-500">5월즈/ 월요일 {{ t('name.zoa') }}/ 스폰지밥</strong>
                - {{ t('name.monday') }}, {{ t('name.zoa') }}
              </li>
              <li>
                <strong class="text-blue-800">맏막즈/ 리막즈/ {{ t('name.zoa') }}진/ 과수원</strong>
                - {{ t('name.soojin') }}, {{ t('name.zoa') }}
              </li>
              <li>
                <strong class="text-red-500">언니즈/ 성인즈/ 언니라인</strong>
                - {{ t('name.soojin') }}, {{ t('name.jiyoon') }}, {{ t('name.monday') }}, {{ t('name.soeun') }}
              </li>
              <li>
                <strong class="text-blue-800">동생즈/ 막내(동생)라인/ 외동즈/ 학생라인/ 산리오 / 뽀송즈</strong>
                - {{ t('name.jaehee') }}, {{ t('name.jihan') }}, {{ t('name.zoa') }}
              </li>
              <li>
                <strong class="text-red-500">주말즈/ 이씨즈/ 이이즈/ 케챱즈/ 유일무이즈</strong>
                - {{ t('name.soojin') }}, {{ t('name.jaehee') }}
              </li>
              <li>
                <strong class="text-blue-800">평일즈</strong>
                - {{ t('name.jiyoon') }}, {{ t('name.monday') }}, {{ t('name.soeun') }}, {{ t('name.jihan') }}, {{ t('name.zoa') }}
              </li>
              <li>
                <strong class="text-red-500">강토즈/ A형즈</strong>
                - {{ t('name.soojin') }}, {{ t('name.jihan') }}
              </li>
              <li>
                <strong class="text-blue-800">행복해지소/ 빌런즈/ 긍굥쌤</strong>
                - {{ t('name.jiyoon') }}, {{ t('name.soeun') }}
              </li>
              <li>
                <strong class="text-red-500">믹나즈</strong>
                - {{ t('name.soojin') }}, {{ t('name.jiyoon') }}, {{ t('name.soeun') }}
              </li>
              <li>
                <strong class="text-blue-800">젤리데이/ 룸메즈</strong>
                - {{ t('name.jaehee') }}, {{ t('name.monday') }}
              </li>
              <li>
                <strong class="text-red-500">쏭아지</strong>
                - {{ t('name.soeun') }}, {{ t('name.zoa') }}, {{ t('name.jiyoon') }}
              </li>
              <li>
                <strong class="text-blue-800">수소즈/ 연습생장기라인즈</strong>
                - {{ t('name.soojin') }}, {{ t('name.soeun') }}
              </li>
              <li>
                <strong class="text-red-500">사랑둥이즈/ ENFJ즈</strong>
                - {{ t('name.jaehee') }}, {{ t('name.zoa') }}
              </li>
              <li>
                <strong class="text-blue-800">짠소금/ 화목즈/ 주토피아즈</strong>
                - {{ t('name.soeun') }}, {{ t('name.jihan') }}
              </li>
              <li>
                <strong class="text-red-500">찰떡즈</strong>
                - {{ t('name.jiyoon') }}, {{ t('name.zoa') }}
              </li>
              <li>
                <strong class="text-blue-800">진지즈/ 식빵즈/ 수지즈</strong>
                - {{ t('name.soojin') }}, {{ t('name.jiyoon') }}
              </li>
              <li>
                <strong class="text-red-500">설탕즈</strong>
                - {{ t('name.soojin') }}, {{ t('name.jihan') }}, {{ t('name.zoa') }}
              </li>
              <li>
                <strong class="text-blue-800">메댄즈</strong>
                - {{ t('name.soojin') }}, {{ t('name.monday') }}, {{ t('name.soeun') }}
              </li>
              <li>
                <strong class="text-red-500">삼백안즈</strong>
                - {{ t('name.soojin') }},{{ t('name.monday') }},{{ t('name.zoa') }}
              </li>
              <li>
                <strong class="text-blue-800">지방즈</strong>
                - {{ t('name.monday') }}, {{ t('name.soeun') }}
              </li>
              <li>
                <strong class="text-red-500">장신즈</strong>
                - {{ t('name.monday') }}, {{ t('name.soeun') }}, {{ t('name.zoa') }}
              </li>
              <li>
                <strong class="text-blue-800">단신즈/ 쪼꼬미즈/ 평균즈</strong>
                - {{ t('name.soojin') }}, {{ t('name.jaehee') }}, {{ t('name.jiyoon') }}, {{ t('name.jihan') }}
              </li>
              <li>
                <strong class="text-red-500">일월즈/ 톰과제리즈</strong>
                - {{ t('name.soojin') }}, {{ t('name.monday') }}
              </li>
              <li>
                <strong class="text-blue-800">예명즈</strong>
                - {{ t('name.jihan') }}, {{ t('name.monday') }}, {{ t('name.zoa') }}
              </li>
              <li>
                <strong class="text-red-500">본명즈</strong>
                - {{ t('name.soojin') }}, {{ t('name.jaehee') }}, {{ t('name.jiyoon') }}, {{ t('name.soeun') }}
              </li>
              <li>
                <strong class="text-blue-800">화채즈</strong>
                - {{ t('name.soojin') }}, {{ t('name.soeun') }}, {{ t('name.jihan') }}
              </li>
              <li>
                <strong class="text-red-500">태극즈</strong>
                - {{ t('name.soeun') }}, {{ t('name.zoa') }}
              </li>
              <li>
                <strong class="text-blue-800">B형즈</strong>
                - {{ t('name.jiyoon') }}, {{ t('name.monday') }}, {{ t('name.soeun') }}, {{ t('name.jaehee') }}
              </li>
            </ul>
          </div>
        </div>
      </div>
      <!-- 3. 外貌 -->
      <div class="collapse w-full collapse-arrow">
        <input type="checkbox" />
        <div
          class="collapse-title text-xl font-extrabold"
          id="s-3"
        >3. {{ t('home.Directory.appearance') }}</div>
        <div class="collapse-content">
          <div class="mx-5">
            <ul class="list-disc">
              <li>멤버 개개인의 외모가 개성있고 예쁘다. 또한 평균 키가 매우 크다.</li>
            </ul>
          </div>
        </div>
      </div>
      <!-- 4. 世界觀 -->
      <div class="collapse w-full collapse-arrow">
        <input type="checkbox" />
        <div
          class="collapse-title text-xl font-extrabold"
          id="s-4"
        >4. {{ t('home.Directory.world View') }}</div>
        <div class="collapse-content">
          <div class="mx-5">
            <ul class="list-disc">
              <li class="pb-4">
                Weeekly依照成員們個別的teaser就具有獨立的世界觀。
                成員們擔當的星期設定(一~日)和象徵天體透過官咖創造神‘D🪐NA(도나)’逐漸向粉絲滿足了對世界觀的好奇心。
              </li>
              <li class="pb-4">
                Jihan的teaser影片《A MESSAGE FROM MARS》中，
                因為Jihan是火星的星主，所以可以從火星向其他成員發送訊息。
                剩下的成員們是受珍-太陽、{{ t('name.monday') }}-月亮、智阭-水星、昭垠-木星、{{ t('name.zoa') }}-金星、在希-土星。
                這邊要注意的一點是，{{ t('name.monday') }}是"月"，與在地球身邊旋轉與其他成員不同。
              </li>
              <li>除此之外世界觀的核心內容如下:</li>
              <div class="pl-8 pb-4">
                <li>成員們已失去了記憶。</li>
                <li>Weeekly成員們為何來到地球呢?</li>
                <li>
                  帶有許多好奇心的月球星主{{ t('name.monday') }}喜歡觀察地球。
                  某一天，發現地球出現問題後向掌管太陽系的受珍報告了這一消息。
                </li>
                <li>
                  從Universe的舞台來看，有著成員們以太陽星主受珍為中心旋 轉的舞蹈。
                  這是以太陽系的移動和行星們的公轉/自轉的模樣來比喻成旋轉木馬。
                </li>
                <li>地球上生活著Daileee和Weeekly，為何地球上的最後一名少女成為了水星主智阭呢?</li>
              </div>
              <li
                class="pb-4"
              >在Zig Zag MV和After School的MV中持續出現的貓和蝸牛代表著重要作用，其中貓的名字在After School的showcase中被確認是Uni。</li>
              <li class="pb-4">
                We Play 第四首歌曲《Uni》是MV中的貓咪，從歌曲的歌詞來看，
                給人一種jump truck載著成員們奔跑的印象。
                從Zig Zag MV中，貓咪背上揹著成員們生活著的學校來看，
                可以推測Uni的角色可能是載成員們回到原本行星當星主。
              </li>
            </ul>
          </div>
        </div>
      </div>
      <!-- 5. 專輯列表 -->
      <div class="collapse w-full collapse-arrow">
        <input type="checkbox" />
        <div
          class="collapse-title text-xl font-extrabold"
          id="s-5"
        >5. {{ t('home.Directory.album List') }}</div>
        <div class="collapse-content">
          <div class="mx-5 flex items-center">
            <div class="w-5">
              <img src="@/assets/images/detail.svg" alt />
            </div>
            <span class="ml-3">
              자세한 내용은
              <a
                href="https://namu.wiki/w/Weeekly/%EC%9D%8C%EB%B0%98%20%EB%AA%A9%EB%A1%9D"
              >Weeekly/음반 목록</a> 문서를 참고하십시오.
            </span>
          </div>
        </div>
      </div>
      <!-- 6. MV -->
      <div class="collapse w-full collapse-arrow">
        <input type="checkbox" />
        <div class="collapse-title text-xl font-extrabold" id="s-6">6. {{ t('home.Directory.MV') }}</div>
        <div class="collapse-content">
          <div class="mx-5 gird">
            <div class="flex items-center pb-4">
              <div class="w-5">
                <img src="@/assets/images/detail.svg" alt />
              </div>
              <span class="ml-3">
                <a
                  href="https://www.kpop-radar.com/Weeekly"
                  class="no-underline hover:underline"
                >위클리(Weeekly) 실시간 뮤직비디오 조회수 추이</a>
              </span>
            </div>

            <!-- table -->
            <div
              class="text-center grid divide-x-1 border-2 border-blue-100 divide-white overflow-auto"
            >
              <div class="bg-blue-100 text-white font-semibold">
                <span>
                  <p class="mt-1">Weeekly MV Youtube 조회수</p>
                  <p class="mb-1">(2021년 08월 19일 PM 7:40 KST 기준)</p>
                </span>
              </div>
              <table class="table-auto border-collapse w-full">
                <tbody class="bg-white">
                  <tr class="bg-blue-100 text-white font-semibold">
                    <td class="border border-gray-200">순위</td>
                    <td class="border border-gray-200">곡명</td>
                    <td class="border border-gray-200">조회수</td>
                    <td class="border border-gray-200">발표일</td>
                    <td class="border border-gray-200">앨범명</td>
                  </tr>
                  <tr>
                    <td class="border border-gray-200 font-semibold">01</td>
                    <td class="border border-gray-200 hover:underline">
                      <a href="https://youtu.be/qfVuRQX0ydQ">After School</a>
                    </td>
                    <td class="border border-gray-200 font-semibold">100,139,378</td>
                    <td class="border border-gray-200">2021년 03월 17일</td>
                    <td class="border border-gray-200">We play</td>
                  </tr>
                  <tr>
                    <td class="border border-gray-200 font-semibold">02</td>
                    <td class="border border-gray-200 hover:underline">
                      <a href="https://youtu.be/DZEOt4pQXXk">Holiday Party</a>
                    </td>
                    <td class="border border-gray-200 font-semibold">21,469,801</td>
                    <td class="border border-gray-200">2021년 08월 04일</td>
                    <td class="border border-gray-200">Play Game : Holiday</td>
                  </tr>
                  <tr>
                    <td class="border border-gray-200 font-semibold">03</td>
                    <td class="border border-gray-200 hover:underline">
                      <a href="https://youtu.be/Moq0aOiTUOA">Tag Me</a>
                    </td>
                    <td class="border border-gray-200 font-semibold">17,823,333</td>
                    <td class="border border-gray-200">2020년 06월 30일</td>
                    <td class="border border-gray-200">We are</td>
                  </tr>
                  <tr>
                    <td class="border border-gray-200 font-semibold">04</td>
                    <td class="border border-gray-200 hover:underline">
                      <a href="https://youtu.be/1FqAoADnId4">Zig Zag</a>
                    </td>
                    <td class="border border-gray-200 font-semibold">16,711,007</td>
                    <td class="border border-gray-200">2020년 10월 13일</td>
                    <td class="border border-gray-200">We can</td>
                  </tr>
                </tbody>
              </table>
            </div>
            <div
              class="mt-4"
            >틱톡 챌린지 및 해외 팬들이 유입되면서 After School의 조회수 증가량 추이가 급격히 상승하는 중이다. 2021년 9월 20일 조회수 1억을 돌파했다.</div>
          </div>
        </div>
      </div>
      <!-- 7. 活動 -->
      <div class="collapse w-full collapse-arrow">
        <input type="checkbox" />
        <div
          class="collapse-title text-xl font-extrabold"
          id="s-6"
        >7. {{ t('home.Directory.activity') }}</div>
        <div class="collapse-content">
          <div class="mx-5 gird">
            <div class="flex items-center pb-4">
              <div class="w-5">
                <img src="@/assets/images/detail.svg" alt />
              </div>
              <span class="ml-3">
                <a
                  href="https://www.kpop-radar.com/Weeekly"
                  class="no-underline hover:underline"
                >자세한 내용은 Weeekly/활동 문서를 참고하십시오.</a>
              </span>
            </div>
          </div>
        </div>
      </div>
      <!-- 7.1 V LIVE -->
      <div class="collapse w-full collapse-arrow">
        <input type="checkbox" />
        <div class="collapse-title text-xl font-extrabold" id="s-6">7.1 V LIVE</div>
        <div class="collapse-content">
          <div class="mx-5 gird">
            <div class="flex items-center pb-4">
              <div class="w-5">
                <img src="@/assets/images/detail.svg" alt />
              </div>
              <span class="ml-3">
                <a
                  href="https://www.kpop-radar.com/Weeekly"
                  class="no-underline hover:underline"
                >자세한 내용은 Weeekly/V LIVE 문서를 참고하십시오.</a>
              </span>
            </div>
          </div>
        </div>
      </div>
      <!-- 7.2 廣告及畫報 -->
      <div class="collapse w-full collapse-arrow">
        <input type="checkbox" />
        <div
          class="collapse-title text-xl font-extrabold"
          id="s-7.2"
        >7.2 {{ t('home.Directory.advertise') }}</div>
        <div class="collapse-content">
          <div class="mx-5 gird">
            <!-- 7.2.1 廣告 -->
            <details>
              <summary
                class="text-xl font-extrabold"
                id="s-7.2.1"
              >7.2.1 {{ t('home.Directory.ads') }}</summary>
              <div class="mx-5 gird">
                <table class="table-auto w-full border border-blue-100 text-center open">
                  <thead class="bg-blue-100 text-white">
                    <tr class="divide-white divide-x">
                      <th>기업명</th>
                      <th>브랜드명</th>
                      <th>분류</th>
                      <th>출연 멤버</th>
                      <th>비고</th>
                    </tr>
                  </thead>
                  <tbody class="bg-white">
                    <tr class="divide-gray-300 divide-x">
                      <td>다비치 안경 체인</td>
                      <td>텐션 7데이 렌즈</td>
                      <td>브랜드 모델</td>
                      <td>전원</td>
                      <td>브랜드송 텐션업</td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </details>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
