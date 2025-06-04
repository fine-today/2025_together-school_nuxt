<template>
  <div>
    <section class="section1">
      <div class="wrap">
        <ul class="favorite-list">
          <li
            class="favorite-item"
            v-for="favoriteItem in favoriteLists"
            :key="favoriteItem.id"
          >
            <a :href="favoriteItem.anchor" class="favorite-anchor">
              <Icon :icon="favoriteItem.icon" />
              <span class="title">{{ favoriteItem.title }}</span>
            </a>
          </li>
        </ul>
      </div>
    </section>

    <section class="section2">
      <div class="wrap">
        <div class="section2-item notice">
          <div class="section2-header">
            <h2>
              공지사항
              <icons class="section2-header-icon notice-icon" icon="notice" />
            </h2>
            <a href="#n" class="more">
              더보기
              <icons class="more-icon" icon="expand" />
            </a>
          </div>

          <div class="notice-list-wrap">
            <ul class="notice-list">
              <li
                class="notice-item"
                v-for="noticeItem in noticeLists"
                :key="noticeItem.id"
              >
                <a :href="noticeItem.anchor" class="notice-title">{{
                  noticeItem.title
                }}</a>
                <span class="notice-date">{{ noticeItem.date }}</span>
              </li>
            </ul>
          </div>
        </div>
        <div class="section2-item video">
          <div class="section2-header">
            <h2>
              영상나눔
              <icons class="section2-header-icon video-icon" icon="video" />
            </h2>
            <a href="#n" class="more">
              더보기
              <icons class="more-icon" icon="expand" />
            </a>
          </div>
          <div class="video-list-wrap">
            <ul class="video-list">
              <li
                class="video-item"
                v-for="videoItem in videoLists"
                :key="videoItem.id"
              >
                <a :href="videoItem.anchor" class="video-item">
                  <div
                    class="thumbnail"
                    v-bind:style="`background: url(${videoItem.thumbnail})`"
                  ></div>
                  <div class="title-wrap">
                    <div class="video-title"></div>
                    <div class="from"></div>
                  </div>
                </a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
import { reactive } from "vue";
import Icon from "@/components/pub/ui/Icons.vue";
const favoriteLists = reactive([
  {
    id: "favorite01",
    title: "정책소개",
    anchor: "#n",
    icon: "mainIntroduce",
  },
  {
    id: "favorite01",
    title: "정책제안",
    anchor: "#n",
    icon: "mainProposal",
  },
  {
    id: "favorite01",
    title: "정책토론",
    anchor: "#n",
    icon: "mainDiscussion",
  },
  {
    id: "favorite01",
    title: "정책답변",
    anchor: "#n",
    icon: "mainAnswer",
  },
  {
    id: "favorite01",
    title: "정책실현",
    anchor: "#n",
    icon: "mainRealization",
  },
]);

const noticeLists = reactive([
  {
    id: "notice1",
    title: "학부모 가이드북 “학부모는 처음이라” E-Book 보기, PDF…",
    date: "4/22",
    anchor: "#n",
  },
  {
    id: "notice2",
    title: "[AI 디지털교과서 활용 수업 콘텐츠 1차 공모전] 입상자 안내",
    date: "4/22",
    anchor: "#n",
  },
  {
    id: "notice3",
    title: "2025 함께동아리 멘토링 프로그램 모집 안내(축구 분야)",
    date: "4/22",
    anchor: "#n",
  },
  {
    id: "notice4",
    title: "청소년 도박, 잃는 건 돈이 아니라 여러분의 미래입니다.",
    date: "4/22",
    anchor: "#n",
  },
  {
    id: "notice4",
    title: "[학원 뺑뺑이 탈출 프로젝트 - 스스로도 잘해요!] 공모전 운영",
    date: "4/22",
    anchor: "#n",
  },
]);

const videoLists = reactive([
  {
    id: "video01",
    title: "맞춤형 학업성취도 자율평가",
    source: "강혜진 박사 한국교육과정평가원",
    anchor: "#n",
    thumbnail: "@/images/main/video01.jpg",
  },
  {
    id: "video02",
    title: "고교학점제 학부모 대상 온라인",
    source: "교육부",
    anchor: "#n",
    thumbnail: "@/images/main/video02.jpg",
  },
]);
</script>

<style scope lang="scss">
.section1 {
  padding: 80px;
}
.favorite-list {
  display: flex;
  text-align: center;
  justify-content: space-between;
  gap: 35px;
}
.favorite-item {
  display: flex;
  width: 100%;
  height: 244px;
  flex: 1;
  border-radius: 30px;
  background-color: #0c8365;
  transition: all 0.2s;
  &:hover {
    background-color: #000a6b;
    box-shadow: 0 0 15px 0 rgba(0, 0, 0, 0.2);
    .favorite-anchor {
    }
  }
  .favorite-anchor {
    display: flex;
    width: 100%;
    height: 100%;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    overflow: hidden;
    border-radius: 30px;
    gap: 20px;
    .svg-icon {
      width: 120px;
      height: 120px;
      border-radius: 50%;
      background-color: #fff;
      display: inline-flex;
      justify-content: center;
      align-items: center;
    }
    .title {
      font-size: 22px;
      color: #fff;
    }
  }
}

.section2 {
  padding: 80px 0;
  background: url(@/public/images/main/notice-bg.png) no-repeat center left;
  .notice {
  }
  .notice-header {
    h2 {
      .notice-icon {
      }
    }
    .more {
      .more-icon {
      }
    }
  }
}
</style>
