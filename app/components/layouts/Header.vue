<script setup>
import { Ellipsis, X } from 'lucide-vue-next'
// import { GitHubIcon } from 'vue3-simple-icons'

// const showMenu = ref(false)
const { title } = useAppConfig()
</script>

<template>
  <section class="pb-6">
    <nav class="container relative z-50 h-24 select-none">
      <div
        class="container relative flex flex-wrap items-center justify-between h-24 px-0 mx-auto overflow-hidden font-medium border-b border-gray-200 md:overflow-visible lg:justify-center"
      >
        <div class="flex items-center justify-start w-1/4 h-full pr-4">
          <a
            href="/"
            :title="title"
            class="flex items-center p-4 px-6 space-x-2 text-xl font-black bg-[#b71918] text-white"
          >
            <svg width="130" height="16" viewBox="0 0 130 16" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M40.932 6.11255H37.3138V9.75578H40.932V6.11255Z" fill="white" />
              <path d="M103.519 12.2875H99.9008V15.9307H103.519V12.2875Z" fill="white" />
              <path d="M13.6258 7.84687C13.6258 1.88333 10.4726 0 5.51782 0H0V15.876H5.11219C10.6976 15.876 13.6258 13.812 13.6258 7.84687ZM9.14424 7.91458C9.14424 11.0677 8.0863 12.1109 5.36145 12.1109H4.41343V3.7651H5.49511C8.22099 3.7651 9.14424 4.98958 9.14424 7.91458Z" fill="white" />
              <path d="M28.9603 15.876V0H24.7708V4.33125C24.7708 5.62448 24.7925 7.73385 24.9071 8.43646C24.568 7.77865 23.1715 5.66927 22.4506 4.69531L18.9831 0H15.1322V15.876H19.3211V11.0229C19.3211 9.72969 19.2979 7.62083 19.1854 6.91771C19.59 7.62083 20.9416 9.66146 21.6398 10.637L25.4015 15.876H28.9603Z" fill="white" />
              <path d="M59.1292 0H54.2647L53.116 4.26354C52.5762 6.2599 51.8103 9.45729 51.5167 10.976C51.2246 9.45729 50.4587 6.23802 49.9189 4.26354L48.7701 0H43.8597L49.2883 15.876H53.7022L59.1292 0Z" fill="white" />
              <path d="M74.0777 15.876V0H69.8872V4.33125C69.8872 5.62448 69.911 7.73385 70.0224 8.43646C69.686 7.77865 68.2895 5.66927 67.5696 4.69531L64.1005 0H60.2496V15.876H64.4391V11.0229C64.4391 9.72969 64.4153 7.62083 64.3034 6.91771C64.7095 7.62083 66.0595 9.66146 66.7578 10.637L70.521 15.876H74.0777Z" fill="white" />
              <path d="M80.9435 0H76.4867V15.876H80.9435V0Z" fill="white" />
              <path d="M97.9005 15.876L92.6087 5.60312L97.3596 0H92.0451L90.7839 1.61042C89.7703 2.90312 88.3955 4.7401 87.7432 5.78437C87.7886 4.62708 87.8092 3.19792 87.8092 1.8599V0H83.3494V15.876H87.8092V11.0906L89.4338 9.11771L92.7212 15.876H97.9005Z" fill="white" />
              <path d="M43.1991 15.876V12.1797H35.2945V3.69635H43.0423V0H30.9698V15.876H43.1991Z" fill="white" />
              <path d="M107.141 0.0682373H111.386V5.66824H111.427C111.808 5.2047 112.29 4.83074 112.873 4.54688C113.438 4.27032 114.196 4.13282 115.147 4.13282C116.188 4.13282 117.082 4.45313 117.828 5.0922C118.568 5.73126 118.945 6.71928 118.959 8.05574V16H114.715V9.93751C114.73 9.2547 114.653 8.70365 114.479 8.28386C114.299 7.8698 113.876 7.66147 113.213 7.66147C112.797 7.64897 112.404 7.78178 112.026 8.06511C111.845 8.21043 111.691 8.43126 111.561 8.7297C111.442 9.04115 111.382 9.4297 111.382 9.89272V16H107.141V0.0682373Z" fill="white" />
              <path d="M129.328 7.98906C129.084 7.94583 128.749 7.92344 128.322 7.92344C126.618 7.89531 125.755 9.06042 125.745 11.4214V16H121.502V4.41615H125.578V6.26875H125.62C125.963 5.57135 126.383 5.03698 126.89 4.66667C127.371 4.31146 127.993 4.13281 128.753 4.13281C129.177 4.13281 129.594 4.19167 130 4.30729" fill="white" />
            </svg>
            <span class="pt-0.5">/ linkovi</span>
          </a>
        </div>

        <div
          class="top-0 left-0 items-start w-full h-full p-4 text-sm bg-gray-900 bg-opacity-50 md:items-center md:w-3/4 md:absolute lg:text-base md:bg-transparent md:p-0 md:relative md:flex"
          :class="{ 'flex fixed': showMenu, 'hidden': !showMenu }"
          @touchmove.prevent
        >
          <div
            class="flex-col w-full h-auto overflow-hidden rounded-lg bg-background md:overflow-visible md:rounded-none md:relative md:flex md:flex-row"
          >
            <a
              href="/"
              :title="title"
              class="inline-flex items-center w-auto h-16 px-4 text-xl font-black leading-none text-gray-900 dark:text-gray-100 md:hidden"
            >
              <span
                class="flex items-center justify-center w-8 h-8 text-white bg-gray-900 rounded-full"
              >
                <img
                  src="/sink.png"
                  :alt="title"
                  class="w-full h-full rounded-full"
                >
              </span>
              <span class="mx-2">{{ title }}</span>
            </a>
            <div class="w-auto mx-4" />
            <div
              class="flex flex-col items-start justify-end w-full pt-4 md:items-center md:flex-row md:py-0"
            >
              <a
                class="rounded text-center transition focus-visible:ring-2 ring-offset-2 ring-gray-200 px-4 py-2 bg-black text-white hover:bg-gray-800 border-2 border-transparent"
                href="/dashboard"
                :title="`${title} Dashboard`"
              >{{ $t('dashboard.title') }}</a>
            </div>
          </div>
        </div>

        <div
          class="absolute right-0 flex flex-col items-center justify-center w-10 h-10 rounded-full cursor-pointer md:hidden hover:bg-muted"
          :class="{ 'right-2': showMenu }"
          @click="showMenu = !showMenu"
        >
          <Ellipsis
            v-show="!showMenu"
            class="w-6 h-6"
          />
          <X
            v-show="showMenu"
            class="w-6 h-6"
          />
        </div>
      </div>
    </nav>
  </section>
</template>
