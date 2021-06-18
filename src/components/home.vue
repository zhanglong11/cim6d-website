<template>
  <div class="home">
    <div class="mouse" v-if="activeIndex !== 4"></div>
    <div class="swiper-container" id="pageRoll">
      <header class="header">
        <div class="wrap">
          <img src="~@/assets/images/logo.png" class="logo" />
          <div class="menu">
            <a
              href="javascript:;"
              @click="sendTo(0)"
              :class="{ active: activeIndex === 0 }"
              >首页</a
            >
            <a
              href="javascript:;"
              @click="sendTo(1)"
              :class="{ active: activeIndex === 1 }"
              >功能介绍</a
            >
            <a
              href="javascript:;"
              @click="sendTo(2)"
              :class="{ active: activeIndex === 2 }"
              >产品特性</a
            >
            <a
              href="javascript:;"
              @click="sendTo(3)"
              :class="{ active: activeIndex === 3 }"
              >案例库</a
            >
            <a
              href="javascript:;"
              @click="sendTo(4)"
              :class="{ active: activeIndex === 4 }"
              >合作伙伴</a
            >
            <a href="javascript:;" @click="modalShow = true">商务合作</a>
            <a href="http://ly.gim6d.com:9912/download/" target="_blank"
              >APP下载</a
            >
          </div>
        </div>
      </header>
      <div class="swiper-wrapper">
        <div class="swiper-slide banner">
          <div class="wrap">
            <div>
              <h2 :class="activeIndex === 0 ? animateList[0][0] : ''">
                智慧工地可视化大屏
              </h2>
              <h3 :class="activeIndex === 0 ? animateList[0][1] : ''">
                进度 质量 安全 成本 尽在掌握
              </h3>
            </div>
          </div>
          <div class="video">
            <div class="video-mask"></div>
            <video
              src="~@/assets/connect-people.mp4"
              poster="~@/assets/video.jpg"
              muted
              loop
              autoplay
              width="100%"
              height="100%"
            ></video>
          </div>
        </div>
        <div class="swiper-slide page2">
          <div class="swiper-container swiper-data" id="swiperData">
            <div class="swiper-wrapper">
              <div class="swiper-slide">
                <div class="wrap bigScreen">
                  <h2 :class="dataSwiperIndex === 0 ? animateList[1][0] : ''">
                    数据<b>可视化</b>
                  </h2>
                  <h3 :class="dataSwiperIndex === 0 ? animateList[1][1] : ''">
                    可视化操作，基于BIM+GIS的模型展示，实现工程大数据可视化管理，实时展示工地上人员考勤打卡的数据，并展示各类监测器的心跳监测数据；同时绘制重要数据的统计图，界面美观专业性强
                  </h3>
                  <div class="ban-img">
                    <img
                      src="~@/assets/images/bigScreen/ban1.png"
                      class="ban"
                      :class="dataSwiperIndex === 0 ? animateList[1][2] : ''"
                    />
                  </div>
                </div>
              </div>
              <div class="swiper-slide">
                <div class="wrap bigScreen">
                  <h2 :class="dataSwiperIndex === 1 ? animateList[1][0] : ''">
                    数据<b>可视化</b>
                  </h2>
                  <h3 :class="dataSwiperIndex === 1 ? animateList[1][1] : ''">
                    可视化操作，基于BIM+GIS的模型展示，实现工程大数据可视化管理，实时展示工地上人员考勤打卡的数据，并展示各类监测器的心跳监测数据；同时绘制重要数据的统计图，界面美观专业性强
                  </h3>
                  <div class="ban-img">
                    <img
                      src="~@/assets/images/bigScreen/ban2.png"
                      class="ban"
                      :class="dataSwiperIndex === 1 ? animateList[1][2] : ''"
                    />
                  </div>
                </div>
              </div>
              <div class="swiper-slide">
                <div class="wrap bigScreen">
                  <h2 :class="dataSwiperIndex === 2 ? animateList[1][0] : ''">
                    数据<b>可视化</b>
                  </h2>
                  <h3 :class="dataSwiperIndex === 2 ? animateList[1][1] : ''">
                    可视化操作，基于BIM+GIS的模型展示，实现工程大数据可视化管理，实时展示工地上人员考勤打卡的数据，并展示各类监测器的心跳监测数据；同时绘制重要数据的统计图，界面美观专业性强
                  </h3>
                  <img
                    src="~@/assets/images/bigScreen/ban3.png"
                    class="ban"
                    :class="dataSwiperIndex === 2 ? animateList[1][2] : ''"
                  />
                </div>
              </div>
              <div class="swiper-slide">
                <div class="wrap bigScreen">
                  <h2 :class="dataSwiperIndex === 3 ? animateList[1][0] : ''">
                    数据<b>可视化</b>
                  </h2>
                  <h3 :class="dataSwiperIndex === 3 ? animateList[1][1] : ''">
                    可视化操作，基于BIM+GIS的模型展示，实现工程大数据可视化管理，实时展示工地上人员考勤打卡的数据，并展示各类监测器的心跳监测数据；同时绘制重要数据的统计图，界面美观专业性强
                  </h3>
                  <img
                    src="~@/assets/images/bigScreen/ban4.png"
                    class="ban"
                    :class="dataSwiperIndex === 3 ? animateList[1][2] : ''"
                  />
                </div>
              </div>
            </div>
            <div class="wrap btn-group">
              <div
                class="swiper-data-btn swiper-data-prev"
                :class="{ disable: dataSwiperIndex === 0 }"
              ></div>
              <div
                class="swiper-data-btn swiper-data-next"
                :class="{ disable: dataSwiperIndex === 3 }"
              ></div>
            </div>
          </div>
        </div>
        <div class="swiper-slide page3">
          <div class="wrap product">
            <h3 :class="activeIndex === 2 ? animateList[2][0] : ''">
              产品特性
            </h3>
            <ul>
              <li
                :class="{
                  active: productIndex === 0,
                  [animateList[2][1]]: activeIndex === 2,
                }"
                @mouseover="productIndex = 0"
              >
                <div class="title">
                  <svg
                    id="组_19"
                    data-name="组 19"
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="39.998"
                    height="38.973"
                    viewBox="0 0 39 38"
                  >
                    <defs>
                      <linearGradient
                        id="linear-gradient"
                        x1="397"
                        y1="2421.11"
                        x2="430.875"
                        y2="2421.11"
                        gradientUnits="userSpaceOnUse"
                      >
                        <stop offset="0" stop-color="#fa3cc1" />
                        <stop offset="0.505" stop-color="#7849e2" />
                        <stop offset="1" stop-color="#0c52fb" />
                      </linearGradient>
                      <linearGradient
                        id="linear-gradient-2"
                        x1="419.063"
                        y1="2428.66"
                        x2="419.063"
                        y2="2400"
                        gradientUnits="userSpaceOnUse"
                      >
                        <stop offset="0" stop-color="#fa3cc1" />
                        <stop offset="0.505" stop-color="#7849e2" />
                        <stop
                          offset="1"
                          stop-color="#0c52fb"
                          stop-opacity="0.549"
                        />
                      </linearGradient>
                    </defs>
                    <path
                      id="形状_4"
                      data-name="形状 4"
                      class="cls-1"
                      d="M428.884,2404.23h-29.9a1.987,1.987,0,0,0-1.984,1.98v22.13a1.987,1.987,0,0,0,1.984,1.98h29.9a1.987,1.987,0,0,0,1.984-1.98v-22.13a1.987,1.987,0,0,0-1.984-1.98h0Zm-0.6,21.71a1.531,1.531,0,0,1-1.437,1.61H406.574l3.55-5.95,4.57,2.2a1.342,1.342,0,0,0,1.638-.4l4.771-5.92a7.38,7.38,0,0,0,3.117-.09c1.356-.49,1.621-0.96,2.415-2.24a4.442,4.442,0,0,0-7.21-5.01,4.391,4.391,0,0,0-.578,5.29l-4.009,4.97-4.671-2.28a1.36,1.36,0,0,0-1.768.58l-5.274,8.85h-2.141a1.53,1.53,0,0,1-1.437-1.61v-17.63a1.7,1.7,0,0,1,.421-1.13,1.368,1.368,0,0,1,1.016-.47h25.868a1.528,1.528,0,0,1,1.437,1.6v17.63Zm-7.872-12.79a2.2,2.2,0,1,1,2.2,2.2,2.194,2.194,0,0,1-2.2-2.2h0Zm8.335,23.25a1.607,1.607,0,0,1-1.605,1.6h-26.41a1.6,1.6,0,1,1,0-3.2h26.41a1.607,1.607,0,0,1,1.605,1.6h0Zm0,0"
                      transform="translate(-397 -2400)"
                    />
                    <path
                      id="圆角矩形_1"
                      data-name="圆角矩形 1"
                      class="cls-2"
                      d="M403.132,2400H435a1,1,0,0,1,1,1v26.65a1,1,0,0,1-1,1H403.132a1,1,0,0,1-1-1V2401A1,1,0,0,1,403.132,2400Z"
                      transform="translate(-397 -2400)"
                    />
                  </svg>

                  全数字化
                </div>
                <div class="product-body">
                  <p>
                    全数字化集成平台，融合项目管理、BIM轻量化运用、物联网、大数据、云计算、边缘计算于一体，实现管理流程数据、BIM数据、物联网数据的底层互通，真正实现数字一体化平台。
                  </p>
                </div>
              </li>
              <li
                :class="{
                  active: productIndex === 1,
                  [animateList[2][2]]: activeIndex === 2,
                }"
                @mouseover="productIndex = 1"
              >
                <div class="title">
                  <svg
                    id="组_16"
                    data-name="组 16"
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="40.001"
                    height="40.001"
                    viewBox="0 0 37 37"
                  >
                    <defs>
                      <linearGradient
                        id="linear-gradient-3"
                        x1="829"
                        y1="2425.5"
                        x2="862"
                        y2="2425.5"
                        gradientUnits="userSpaceOnUse"
                      >
                        <stop offset="0" stop-color="#fa3cc1" />
                        <stop offset="0.505" stop-color="#7849e2" />
                        <stop offset="1" stop-color="#0c52fb" />
                      </linearGradient>
                      <linearGradient
                        id="linear-gradient-4"
                        x1="849.788"
                        y1="2438"
                        x2="849.212"
                        y2="2405"
                        gradientUnits="userSpaceOnUse"
                      >
                        <stop offset="0" stop-color="#0c52fb" />
                        <stop offset="0.495" stop-color="#7849e2" />
                        <stop
                          offset="1"
                          stop-color="#fa3cc1"
                          stop-opacity="0.02"
                        />
                      </linearGradient>
                    </defs>
                    <path
                      id="形状_5"
                      data-name="形状 5"
                      class="cls-3"
                      d="M845.5,2419.01a6.49,6.49,0,1,0,6.509,6.49,6.505,6.505,0,0,0-6.509-6.49h0Zm0,10.71a4.22,4.22,0,1,1,4.235-4.22,4.23,4.23,0,0,1-4.235,4.22h0Zm15.664-1.61-2.108-1.22a13.617,13.617,0,0,0,.071-1.39,13.765,13.765,0,0,0-.071-1.39l2.108-1.22a1.668,1.668,0,0,0,.613-2.28l-3.894-6.72a1.676,1.676,0,0,0-2.287-.61l-2.108,1.21a13.349,13.349,0,0,0-2.42-1.4v-2.42a1.674,1.674,0,0,0-1.674-1.67h-7.787a1.674,1.674,0,0,0-1.674,1.67v2.42a13.963,13.963,0,0,0-2.42,1.4l-2.108-1.21a1.676,1.676,0,0,0-2.287.61l-3.894,6.72a1.668,1.668,0,0,0,.613,2.28l2.108,1.22a13.642,13.642,0,0,0,0,2.78l-2.108,1.22a1.668,1.668,0,0,0-.613,2.28l3.894,6.72a1.676,1.676,0,0,0,2.287.61l2.108-1.21a13.963,13.963,0,0,0,2.42,1.4v2.42a1.674,1.674,0,0,0,1.674,1.67h7.787a1.674,1.674,0,0,0,1.674-1.67v-2.42a13.963,13.963,0,0,0,2.42-1.4l2.108,1.21a1.676,1.676,0,0,0,2.287-.61l3.894-6.72a1.668,1.668,0,0,0-.613-2.28h0Zm-4.95,7.35-1.932-1.11a1.676,1.676,0,0,0-1.857.12,11.4,11.4,0,0,1-2.6,1.5,1.659,1.659,0,0,0-1.033,1.54v2.22h-6.587v-2.22a1.66,1.66,0,0,0-1.033-1.54,11.4,11.4,0,0,1-2.6-1.5,1.678,1.678,0,0,0-1.858-.12l-1.931,1.11-3.293-5.69,1.93-1.11a1.661,1.661,0,0,0,.823-1.66,11.45,11.45,0,0,1-.1-1.5,11.626,11.626,0,0,1,.1-1.5,1.659,1.659,0,0,0-.823-1.66l-1.93-1.11,3.293-5.69,1.931,1.11a1.678,1.678,0,0,0,1.858-.12,11.4,11.4,0,0,1,2.6-1.5,1.66,1.66,0,0,0,1.033-1.54v-2.22h6.587v2.22a1.66,1.66,0,0,0,1.033,1.54,11.347,11.347,0,0,1,2.6,1.5,1.676,1.676,0,0,0,1.857.12l1.931-1.11,3.294,5.69-1.931,1.11a1.661,1.661,0,0,0-.823,1.66,11.413,11.413,0,0,1,0,3,1.659,1.659,0,0,0,.823,1.66l1.931,1.11Zm0,0"
                      transform="translate(-829 -2405)"
                    />
                    <path
                      id="形状_5_拷贝"
                      data-name="形状 5 拷贝"
                      class="cls-4"
                      d="M865.163,2424.11l-2.108-1.22a13.617,13.617,0,0,0,.071-1.39,13.765,13.765,0,0,0-.071-1.39l2.108-1.22a1.668,1.668,0,0,0,.613-2.28l-3.894-6.72a1.676,1.676,0,0,0-2.287-.61l-2.108,1.21a13.374,13.374,0,0,0-2.419-1.4v-2.42a1.675,1.675,0,0,0-1.675-1.67h-7.787a1.674,1.674,0,0,0-1.674,1.67v2.42a13.963,13.963,0,0,0-2.42,1.4l-2.108-1.21a1.676,1.676,0,0,0-2.287.61l-3.894,6.72a1.668,1.668,0,0,0,.613,2.28l2.108,1.22a13.642,13.642,0,0,0,0,2.78l-2.108,1.22a1.668,1.668,0,0,0-.613,2.28l3.894,6.72a1.676,1.676,0,0,0,2.287.61l2.108-1.21a13.963,13.963,0,0,0,2.42,1.4v2.42a1.674,1.674,0,0,0,1.674,1.67h7.787a1.675,1.675,0,0,0,1.675-1.67v-2.42a13.992,13.992,0,0,0,2.419-1.4l2.108,1.21a1.676,1.676,0,0,0,2.287-.61l3.894-6.72a1.668,1.668,0,0,0-.613-2.28h0Zm-4.951,7.35"
                      transform="translate(-829 -2405)"
                    />
                  </svg>

                  新兴管理模式
                </div>
                <div class="product-body">
                  <p>
                    基于CIM6D底板分布式统一数据库，能实现所有参建方协同工作基础上的项目全生寿命周期管理，项目管理做到横向到边，竖向到底，天然适应EPC、PPC、全过程咨询等各类新兴项目管理模式
                  </p>
                </div>
              </li>
              <li
                :class="{
                  active: productIndex === 2,
                  [animateList[2][3]]: activeIndex === 2,
                }"
                @mouseover="productIndex = 2"
              >
                <div class="title">
                  <svg
                    id="组_17"
                    data-name="组 17"
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="40.001"
                    height="37.648"
                    viewBox="0 0 34 32"
                  >
                    <defs>
                      <linearGradient
                        id="linear-gradient-5"
                        x1="19"
                        y1="28"
                        x2="19"
                        gradientUnits="userSpaceOnUse"
                      >
                        <stop offset="-0.165" stop-color="#7949e2" />
                        <stop offset="-0.161" stop-color="#7949e2" />
                        <stop
                          offset="1.165"
                          stop-color="#1052fa"
                          stop-opacity="0"
                        />
                      </linearGradient>
                      <linearGradient
                        id="linear-gradient-6"
                        x1="1279"
                        y1="2426"
                        x2="1309"
                        y2="2426"
                        gradientUnits="userSpaceOnUse"
                      >
                        <stop offset="0" stop-color="#fa3cc1" />
                        <stop offset="0.505" stop-color="#7849e2" />
                        <stop offset="1" stop-color="#0c52fb" />
                      </linearGradient>
                    </defs>
                    <rect
                      id="圆角矩形_2"
                      data-name="圆角矩形 2"
                      class="cls-5"
                      x="4"
                      width="30"
                      height="28"
                      rx="2"
                      ry="2"
                    />
                    <path
                      id="形状_6"
                      data-name="形状 6"
                      class="cls-6"
                      d="M1307.32,2441h-26.64a1.677,1.677,0,0,1-1.68-1.68v-4.7a1.675,1.675,0,0,1,1.68-1.67h26.64a1.675,1.675,0,0,1,1.68,1.67v4.7a1.677,1.677,0,0,1-1.68,1.68h0Zm-0.33-5.54a0.5,0.5,0,0,0-.51-0.5h-24.96a0.5,0.5,0,0,0-.51.5v0.51h19.27a1.005,1.005,0,1,1,0,2.01h-19.27v0.5a0.512,0.512,0,0,0,.51.51h24.96a0.512,0.512,0,0,0,.51-0.51v-3.02Zm0.33-5.43h-26.64a1.677,1.677,0,0,1-1.68-1.68v-4.7a1.677,1.677,0,0,1,1.68-1.68h26.64a1.677,1.677,0,0,1,1.68,1.68v4.7a1.677,1.677,0,0,1-1.68,1.68h0Zm-0.33-5.54a0.5,0.5,0,0,0-.51-0.5h-24.96a0.5,0.5,0,0,0-.51.5v0.5h10.93a1.01,1.01,0,0,1,0,2.02h-10.93v0.5a0.5,0.5,0,0,0,.51.5h24.96a0.5,0.5,0,0,0,.51-0.5v-3.02Zm0.33-5.44h-26.64a1.675,1.675,0,0,1-1.68-1.67v-4.7a1.677,1.677,0,0,1,1.68-1.68h26.64a1.677,1.677,0,0,1,1.68,1.68v4.7a1.675,1.675,0,0,1-1.68,1.67h0Zm-0.33-5.53a0.512,0.512,0,0,0-.51-0.51h-24.96a0.512,0.512,0,0,0-.51.51v0.5h22.15a1.005,1.005,0,1,1,0,2.01h-22.15v0.51a0.51,0.51,0,0,0,.51.5h24.96a0.51,0.51,0,0,0,.51-0.5v-3.02Zm0,0"
                      transform="translate(-1279 -2409)"
                    />
                  </svg>

                  进度驱动数据
                </div>
                <div class="product-body">
                  <p>
                    以进度为主轴，从任务自动分发开始实现数据驱动。通过打通BIM数据、物联网数据和业务管理流程数据，结合AI和大数据云计算，实现项目基础数据智能收集、分析和计算，达到项目管理减员增效、智能化的效果。
                  </p>
                </div>
              </li>
              <li
                :class="{
                  active: productIndex === 3,
                  [animateList[2][4]]: activeIndex === 2,
                }"
                @mouseover="productIndex = 3"
              >
                <div class="title">
                  <svg
                    id="组_18"
                    data-name="组 18"
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="40.001"
                    height="37.648"
                    viewBox="0 0 34 32"
                  >
                    <defs>
                      <linearGradient
                        id="linear-gradient-7"
                        x1="19"
                        y1="28"
                        x2="19"
                        gradientUnits="userSpaceOnUse"
                      >
                        <stop offset="-0.165" stop-color="#7949e2" />
                        <stop offset="-0.161" stop-color="#7949e2" />
                        <stop
                          offset="1.165"
                          stop-color="#1052fa"
                          stop-opacity="0"
                        />
                      </linearGradient>
                      <linearGradient
                        id="linear-gradient-8"
                        x1="1729"
                        y1="2426"
                        x2="1759"
                        y2="2426"
                        gradientUnits="userSpaceOnUse"
                      >
                        <stop offset="0" stop-color="#fa3cc1" />
                        <stop offset="0.505" stop-color="#7849e2" />
                        <stop offset="1" stop-color="#0c52fb" />
                      </linearGradient>
                    </defs>
                    <rect
                      id="圆角矩形_2_拷贝"
                      data-name="圆角矩形 2 拷贝"
                      class="cls-7"
                      x="4"
                      width="30"
                      height="28"
                      rx="2"
                      ry="2"
                    />
                    <path
                      id="形状_7"
                      data-name="形状 7"
                      class="cls-8"
                      d="M1757.8,2411h-27.6a1.2,1.2,0,0,0-1.2,1.2v27.6a1.2,1.2,0,0,0,1.2,1.2h27.6a1.2,1.2,0,0,0,1.2-1.2v-27.6a1.2,1.2,0,0,0-1.2-1.2h0Zm-1.5,27.3h-24.6v-24.6h24.6v24.6Zm-20.07-11.85h1.9a0.258,0.258,0,0,0,.26-0.26v-2.95a1.332,1.332,0,0,1,1.33-1.34h7.71v2a0.251,0.251,0,0,0,.41.2l4.09-3.21a0.254,0.254,0,0,0,0-.4l-4.09-3.22a0.254,0.254,0,0,0-.41.2v2.01h-7.72a3.743,3.743,0,0,0-3.74,3.75v2.96a0.258,0.258,0,0,0,.26.26h0Zm-0.16,5.06,4.09,3.21a0.254,0.254,0,0,0,.41-0.2v-2h7.72a3.741,3.741,0,0,0,3.73-3.75v-2.96a0.256,0.256,0,0,0-.25-0.26h-1.9a0.265,0.265,0,0,0-.26.26v2.96a1.323,1.323,0,0,1-1.33,1.33h-7.71v-2a0.254,0.254,0,0,0-.41-0.2l-4.09,3.21a0.254,0.254,0,0,0,0,.4h0Zm0,0"
                      transform="translate(-1729 -2409)"
                    />
                  </svg>

                  运行环境稳定
                </div>
                <div class="product-body">
                  <p>
                    搭配自主知识产权的BF-box,通过边缘计算技术，大大提高平台在BIM.IOT等海量数据交互时的快速稳定，减少平台对网络环境的依赖；全面兼容各种数据格式及硬件接口，能适应各种新旧项目复杂的应用环境。
                  </p>
                </div>
              </li>
            </ul>
          </div>
        </div>
        <div class="swiper-slide page4">
          <div class="wrap case">
            <ul>
              <li>
                <div
                  class="case-icon case-icon1"
                  :class="{
                    active: caseIndex === 0,
                    [animateList[3][0]]: activeIndex === 3,
                  }"
                  @mousemove="caseIndex = 0"
                >
                  <p class="title">中建八局开元大桥改建二期项目</p>
                  <p class="desc">中建八局开元大桥</p>
                  <a href="#">
                    了解详情
                    <img src="~@/assets/images/case/case-arrow.png" />
                  </a>
                </div>
                <div
                  class="case-icon case-icon2"
                  :class="{
                    active: caseIndex === 1,
                    [animateList[3][1]]: activeIndex === 3,
                  }"
                  @mousemove="caseIndex = 1"
                >
                  <p class="title">中建八局开元大桥改建二期项目</p>
                  <p class="desc">中建八局开元大桥</p>
                  <a href="#">
                    了解详情
                    <img src="~@/assets/images/case/case-arrow.png" />
                  </a>
                </div>
              </li>
              <li>
                <div
                  class="case-icon case-icon3"
                  :class="{
                    active: caseIndex === 2,
                    [animateList[3][2]]: activeIndex === 3,
                  }"
                  @mousemove="caseIndex = 2"
                >
                  <p class="title">中建八局开元大桥改建二期项目</p>
                  <p class="desc">中建八局开元大桥</p>
                  <a href="#">
                    了解详情
                    <img src="~@/assets/images/case/case-arrow.png" />
                  </a>
                </div>
                <div class="case-center">
                  <div
                    class="case-icon case-icon4"
                    :class="{
                      active: caseIndex === 3,
                      [animateList[3][3]]: activeIndex === 3,
                    }"
                    @mousemove="caseIndex = 3"
                  >
                    <p class="title">中建八局开元大桥</p>
                    <p class="desc">中建八局开元大桥</p>
                    <a href="#">
                      了解详情
                      <img src="~@/assets/images/case/case-arrow.png" />
                    </a>
                  </div>
                  <div
                    class="case-icon case-icon5"
                    :class="{
                      active: caseIndex === 4,
                      [animateList[3][4]]: activeIndex === 3,
                    }"
                    @mousemove="caseIndex = 4"
                  >
                    <p class="title">中建八局开元大桥</p>
                    <p class="desc">中建八局开元大桥</p>
                    <a href="#">
                      了解详情
                      <img src="~@/assets/images/case/case-arrow.png" />
                    </a>
                  </div>
                </div>
              </li>
              <li>
                <div
                  class="case-icon case-icon6"
                  :class="{
                    active: caseIndex === 5,
                    [animateList[3][5]]: activeIndex === 3,
                  }"
                  @mousemove="caseIndex = 5"
                >
                  <p class="title">中建八局开元大桥改建二期项目</p>
                  <p class="desc">中建八局开元大桥</p>
                  <a href="#">
                    了解详情
                    <img src="~@/assets/images/case/case-arrow.png" />
                  </a>
                </div>
              </li>
            </ul>
          </div>
        </div>
        <div class="swiper-slide page5">
          <div class="link">
            <p
              class="title"
              :class="{ [animateList[4][0]]: activeIndex === 4 }"
            >
              合作伙伴
            </p>
            <div class="wrap">
              <img
                src="~@/assets/images/link1.jpg"
                :class="{ [animateList[4][1]]: activeIndex === 4 }"
              />
              <img
                src="~@/assets/images/link2.jpg"
                :class="{ [animateList[4][2]]: activeIndex === 4 }"
              />
              <img
                src="~@/assets/images/link3.jpg"
                :class="{ [animateList[4][3]]: activeIndex === 4 }"
              />
              <img
                src="~@/assets/images/link4.jpg"
                :class="{ [animateList[4][4]]: activeIndex === 4 }"
              />
            </div>
          </div>
          <footer class="footer">
            <div class="wrap footer-link">
              <div class="footer-left">
                <ul>
                  <li>
                    <b>产品中心</b>
                    <p>
                      <a href="javascript:;" @click="sendTo(1)">功能介绍</a>
                      <a href="javascript:;" @click="sendTo(2)">产品特性</a>
                      <a href="javascript:;" @click="sendTo(3)">案例库</a>
                      <a href="javascript:;" @click="sendTo(4)">合作伙伴</a>
                    </p>
                  </li>
                  <li>
                    <b>下载&支持</b>
                    <p>
                      <a href="#">下载软件</a>
                      <a href="#">产品目类</a>
                      <a href="#">售后服务</a>
                    </p>
                  </li>
                  <li>
                    <b>关于我们</b>
                    <p>
                      <a href="#">品牌介绍</a>
                      <a href="#">企业文化</a>
                      <a href="#">生产能力</a>
                      <a href="#">联系我们</a>
                    </p>
                  </li>
                  <li>
                    <b>联系我们</b>
                    <p>
                      联系电话 400-600-8867<br />
                      企业邮箱 bd@BIMfish.com<br />
                      企业官网 WWW.BIMfish.com<br />
                      总部地址 武汉市洪山区珞喻路889-1号融众国际1708室
                    </p>
                  </li>
                </ul>
              </div>
              <div class="footer-right">
                <p :class="{ [animateList[5][0]]: activeIndex === 4 }">
                  <img src="~@/assets/images/ewm1.jpg" />
                  <span>扫一扫关注公众号</span>
                </p>
                <p :class="{ [animateList[5][1]]: activeIndex === 4 }">
                  <img src="~@/assets/images/ewm2.jpg" />
                  <span>扫一扫关注公众号</span>
                </p>
              </div>
            </div>
            <div class="wrap copy">
              &copy;Copyrights比目鱼科技比目鱼（北京）数字科技有限公司<a
                href="https://beian.miit.gov.cn/#/Integrated/index"
                target="_blank"
                >粤ICP备19061555号</a
              >
            </div>
          </footer>
        </div>
      </div>
      <!-- Add Pagination -->
      <div class="swiper-pagination" id="pageRollPagination"></div>
    </div>
    <!-- 商务合作 start -->
    <div class="modal" :class="{ open: modalShow }">
      <div class="modal-mask" :class="{ [modalAnimate[0]]: modalShow }"></div>
      <div class="modal-con" :class="{ [modalAnimate[1]]: modalShow }">
        <div class="modal-title">
          <b>商务合作</b>
          <span class="close" @click="modalShow = false"></span>
        </div>
        <div class="modal-body">
          <div class="form-item">
            <label>姓名</label>
            <input placeholder="请输入姓名" />
          </div>
          <div class="form-item">
            <label>手机号</label>
            <input placeholder="请输入手机号" />
          </div>
          <div class="form-item">
            <label>需求描述</label>
            <textarea placeholder="请输入需求描述" rows="5"></textarea>
          </div>
          <div class="form-item">
            <button @click="modalShow = false">提交</button>
          </div>
        </div>
      </div>
    </div>
    <!-- 商务合作 end -->
  </div>
</template>

<script>
import "animate.css";
import Swiper from "swiper/bundle";
import "swiper/swiper-bundle.css";
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      activeIndex: 0,
      swiperView: null,
      animateList: [
        [
          "animate__animated animate__backInDown",
          "animate__animated animate__zoomInRight animate__delay-400ms",
        ],
        [
          "animate__animated animate__fadeInDown",
          "animate__animated animate__fadeInUp animate__delay-200ms",
          "animate__animated animate__fadeIn",
        ],
        [
          "animate__animated animate__fadeInDown",
          "animate__animated animate__fadeInUp animate__delay-200ms",
          "animate__animated animate__fadeInUp animate__delay-400ms",
          "animate__animated animate__fadeInUp animate__delay-600ms",
          "animate__animated animate__fadeInUp animate__delay-800ms",
        ],
        [
          "animate__animated animate__fadeIn animate__delay-200ms",
          "animate__animated animate__fadeIn animate__delay-400ms",
          "animate__animated animate__fadeIn animate__delay-600ms",
          "animate__animated animate__fadeIn animate__delay-800ms",
          "animate__animated animate__fadeIn animate__delay-1s",
          "animate__animated animate__fadeIn animate__delay-1200ms",
        ],
        [
          "animate__animated animate__fadeInDown",
          "animate__animated animate__fadeInUp animate__delay-200ms",
          "animate__animated animate__fadeInUp animate__delay-400ms",
          "animate__animated animate__fadeInUp animate__delay-600ms",
          "animate__animated animate__fadeInUp animate__delay-800ms",
        ],
        [
          "animate__animated animate__zoomIn animate__delay-200ms",
          "animate__animated animate__zoomIn animate__delay-400ms",
        ],
      ],
      dataSwiperView: null,
      dataSwiperIndex: 0,
      productIndex: 0,
      caseIndex: 0,
      modalShow: false,
      modalAnimate: [
        "animate__animated animate__fadeIn",
        "animate__animated animate__zoomInUp animate__delay-200ms animate__faster",
      ],
    };
  },
  mounted() {
    this.init();
  },
  methods: {
    // 初始化
    init() {
      this.swiperView = new Swiper("#pageRoll", {
        direction: "vertical",
        slidesPerView: 1,
        spaceBetween: 30,
        mousewheel: true,
        // autoplay: {
        //   delay: 15000,
        //   disableOnInteraction: false,
        // },
        // pagination: {
        //   el: "#pageRollPagination",
        //   type: "bullets",
        //   clickable: true,
        // },
      });
      this.swiperView.on("slideChange", (e) => {
        let index = e.activeIndex;
        if (index === 1) {
          this.dataSwiperIndex = 0;
          this.dataSwiperView.slideTo(0, 500);
        }
        this.changeSwiper(index);
      });

      this.dataSwiperView = new Swiper("#swiperData", {
        direction: "horizontal",
        slidesPerView: 1,
        spaceBetween: 30,
        mousewheel: true,
        navigation: {
          nextEl: ".swiper-data-next",
          prevEl: ".swiper-data-prev",
        },
        autoplay: {
          delay: 3000,
          disableOnInteraction: false,
        },
      });
      this.dataSwiperView.on("slideChange", (e) => {
        let index = e.activeIndex;
        this.dataSwiperIndex = index;
      });
    },
    // 页码改变
    changeSwiper(index) {
      this.activeIndex = index;
    },
    // 跳转页面
    sendTo(index) {
      this.swiperView.slideTo(index, 500);
    },
  },
};
</script>
<style lang="less">
@import url("./home");
</style>
