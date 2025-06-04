<template>
  <div class="gnb">
    <div class="wrap">
      <div class="color-mode" :class="colorMode ? 'bright' : 'dark'">
        <div class="input">
          <input type="checkbox" id="color-mode" v-model="colorMode" />
          <label for="color-mode">
            <Icons icon="modeDark" class="bright-icon" />
            <Icons icon="modeBright" class="dark-icon" />
            <span class="circle"></span>
            {{ colorMode ? "기본 컬러 모드" : "다크모드" }}</label
          >
        </div>
      </div>

      <div class="gnb-options">
        <span class="zoom-option">
          <span class="zoom-title"> 글자·화면 표시</span>
          <button type="button" class="zoom-btn reduce">
            화면 축소하기<Icons icon="reduce" />
          </button>
          <button type="button" class="zoom-btn expand">
            화면 확대하기 화면 축소하기<Icons icon="expand" />
          </button>
        </span>
        <button href="#n" class="braille-btn braille-down">
          전자점자다운로드 화면 축소하기<Icons icon="brailleDown" />
        </button>
        <button type="button" class="braille-btn braille-viewer">
          전자점자뷰어보기(새창열림)<Icons icon="brailleViewer" />
        </button>
      </div>
    </div>
  </div>
  <div class="lnb">
    <div class="wrap">
      <h1 class="logo">
        <a href="#n" class="logo-anchor">
          <Icons icon="logo" />
        </a>
      </h1>

      <div class="search">
        <span class="input">
          <input type="text" placeholder="검색어를 입력하세요" />
          <span class="search-btns">
            <button type="button" class="voice-btn">
              <Icons icon="voice" />
            </button>
            <button type="button" class="search-btn">
              <Icons icon="search" /></button
          ></span>
        </span>
      </div>

      <ul class="login-box">
        <li class="login-item">
          <a href="#n" class="login-anchor">
            <Icons icon="login" />
            <span class="title">로그인</span>
          </a>
        </li>
        <li class="login-item">
          <a href="#n" class="login-anchor">
            <Icons icon="logout" />
            <span class="title">로그아웃</span>
          </a>
        </li>
        <li class="login-item">
          <a href="#n" class="login-anchor">
            <Icons icon="join" />
            <span class="title">회원가입</span>
          </a>
        </li>
        <li class="login-item">
          <a href="#n" class="login-anchor">
            <Icons icon="language" />
            <span class="title">언어선택</span>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import Icons from "/components/pub/ui/Icons.vue";
const colorMode = ref(true);
</script>

<style scoped lang="scss">
.color-mode {
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  width: 115px;
  height: 54px;
  background-color: #0c8365;
  box-sizing: border-box;
  position: relative;
  &.dark {
    .input input {
      & + label {
        border-color: #000;
        .circle {
          transform: translateX(40px);
          border-color: #000;
        }
        .svg-icon {
          color: #000;
          &.bright-icon {
            opacity: 0.3;
          }
        }
      }
    }
  }
  &.bright {
    .input input {
      & + label {
        .svg-icon.dark-icon {
          opacity: 0.3;
        }
      }
    }
  }
  .input {
    display: inline-block;
    position: relative;
    width: 80px;
    height: 40px;

    input {
      position: absolute;
      width: 12px;
      height: 12px;
      opacity: 0;
      left: 0;
      top: 0;
      & + label {
        cursor: pointer;
        width: 100%;
        height: 100%;
        left: 0;
        top: 0;
        display: inline-block;
        position: absolute;
        border-radius: 30px;
        border: 2px solid #fff;
        font-size: 0;
        line-height: 0;
        .circle,
        .svg-icon {
          display: inline-flex;
          position: absolute;
          left: 4px;
          top: 4px;
          align-items: center;
          justify-content: center;
          width: 28px;
          height: 28px;
          transition: all 0.2s;
        }
        .circle {
          border-radius: 50%;
          border: 2px solid #fff;
        }
        .svg-icon {
          color: #fff;
        }
        .svg-icon.dark-icon {
          left: auto;
          right: 4px;
        }
      }
      &:checked + label {
        i {
        }
      }
    }
  }
}
.gnb-options {
  gap: 6px;
  display: flex;
  align-items: center;
  .zoom-option {
    display: flex;
    align-items: center;
    margin-right: 9px;
    .zoom-title {
      color: #666;
      font-size: 18px;
      line-height: 1;
      margin-right: 3px;
    }
    .zoom-btn {
      border: 1px solid #ddd;
      font-size: 0;
      line-height: 0;
      height: 22px;
      &.reduce {
        border-radius: 6px 0 0 6px;
        border-right: 0;
        width: 24px;
      }
      &.expand {
        border-radius: 0 6px 6px 0;
        width: 25px;
      }
    }
  }
  .braille-btn {
    width: 39px;
    height: 37px;
    font-size: 0;
    line-height: 0;
    border: 1px solid #ddd;
    border-radius: 10px;
  }
}
.lnb {
  > .wrap {
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: relative;
    height: 142px;
  }
  .logo {
    .logo-anchor {
    }
    .svg-icon {
    }
  }
  .search {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    .input {
      display: inline-flex;
      align-items: center;
      border-radius: 50px;
      width: 445px;
      height: 60px;
      border: 3px solid #000a6b;
      padding: 10px 80px 10px 26px;
      input {
        font-size: 20px;
        &::placeholder {
          color: #999;
        }
      }
      .search-btns {
        display: inline-flex;
        justify-content: center;
        align-items: center;
        position: absolute;
        right: 7px;
        gap: 10px;
        button {
          display: inline-flex;
          justify-content: center;
          align-items: center;
        }
      }
      .voice-btn {
        width: 27px;
        height: 27px;
      }
      .search-btn {
        width: 48px;
        height: 48px;
        border-radius: 50%;
        background-color: #000a6b;
      }
    }
  }
  .login-box {
    display: inline-flex;
    align-items: center;
    gap: 21px;
    .login-item {
      display: inline-flex;
      align-items: center;
      position: relative;
      &::after {
        display: block;
        position: absolute;
        right: -10px;
        height: 20px;
        width: 1px;
        top: 17px;
        background-color: #cdcdcd;
      }
      &:last-child::after {
        display: none;
      }
      .login-anchor {
        display: inline-flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        gap: 6px;
        .svg-icon {
          width: 35px;
          height: 35px;
        }
        .title {
          font-size: 16px;
          line-height: 1;
          color: #666;
        }
      }
    }
  }
}
</style>
