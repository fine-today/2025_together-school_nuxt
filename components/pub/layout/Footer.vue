<template>
  <div>
    <footer id="footer" class="footer">
      <div class="footer-con">
        <div class="footer-line anchor-line">
          <div class="wrap">
            <ul class="footer-anchor-list">
              <li class="footer-anchor-item">
                <a href="#n" class="footer-anchor">이용약관</a>
              </li>
              <li class="footer-anchor-item safety">
                <a href="#n" class="footer-anchor">개인정보처리방침</a>
              </li>
              <li class="footer-anchor-item">
                <a href="#n" class="footer-anchor">청소년 보호정책</a>
              </li>
              <li class="footer-anchor-item">
                <a href="#n" class="footer-anchor">함께학교란?</a>
              </li>
            </ul>
            <ul class="sns-list">
              <li class="sns-item play-store">
                <a href="#n" class="sns-anchor">안드로이드 앱 다운로드</a>
              </li>
              <li class="sns-item app-store">
                <a href="#n" class="sns-anchor">애플 앱 다운로드</a>
              </li>
              <li class="sns-item instagram">
                <a href="#n" class="sns-anchor">인스타그램 바로가기</a>
              </li>
              <li class="sns-item youtube">
                <a href="#n" class="sns-anchor">유튜브 바로가기기</a>
              </li>
              <!--<li class="sns-item btn">
                <a href="#n" class="sns-anchor"
                  ><span>함께학교 지식샘터</span></a
                >
              </li>-->
            </ul>
          </div>
        </div>
        <div class="footer-line">
          <div class="wrap">
            <ul class="logo-list">
              <li class="logo-item">
                <a href="#n" class="logo-anchor" target="_blank" title="새창">
                  <NuxtImg src="/images/common/logo-ebs.png" alt="EBS 로고" />
                </a>
              </li>
              <li class="logo-item">
                <a href="#n" class="logo-anchor" target="_blank" title="새창">
                  <NuxtImg
                    src="/images/common/logo-edu.png"
                    alt="교육부 로고"
                  />
                </a>
              </li>
            </ul>
            <div class="footer-info-list">
              <span class="footer-info-item"
                >30119 세종특별자치시 갈매로 408, 14동 정부세종청사 교육부</span
              >
              <span class="footer-info-item">사업자등록번호 102-83-00181</span
              ><br />
              <span class="footer-info-item"
                >10393 경기도 고양시 일산동구 한류월드로 281
                한국교육방송공사</span
              >
              <span class="footer-info-item">사업자등록번호 : 229-82-01343</span
              ><br />
              <span class="footer-info-item">이용문의 : hotline@ebs.co.kr</span>
              <span class="footer-info-item">고객센터 : 1588-1580</span>
              <span class="footer-info-item">부가통신사업신고 : 10077</span>
              <span class="footer-info-item"
                >통신판매업신고 : 2017-고양일산동-1415</span
              >
              <div class="footer-info-item">
                Copyright ⓒ 교육부 &amp; EBS All Rights Reserved.
              </div>
            </div>
          </div>
        </div>
        <div class="footer-cert">
          <div class="wrap">
            <div class="footer-cert-logo">
              <a href="#n" class="footer-cert-anchor">
                <NuxtImg
                  src="/images/common/logo-ismsp.png"
                  alt="정보보호 및 개인정보보호 관리체계 인증 ISMS·P - Personal Information &amp; Information Security Monagement System"
                />
              </a>
            </div>
            <p class="footer-cert-text">
              [인증범위] EBS 교육 포털 웹서비스 시스템 운영<br />
              [유효기간] 2025.04.16 ~ 2028.04.15
            </p>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup></script>

<style scope lang="scss">
@import url("/public/css/footer.scss");
</style>
