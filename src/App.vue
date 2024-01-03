<script setup lang="ts">
import FacebookSquareSVG from "./assets/svg/facebook_square.svg";
import FolderOpenSVG from "./assets/svg/folder_open.svg";
import GithubSVG from "./assets/svg/github.svg";
import InfoSVG from "./assets/svg/info.svg";
import LinkedinSquareSVG from "./assets/svg/linkedin_square.svg";
import ButtonCard from "./components/ButtonCard.vue";
import GithubCorner from "./components/GithubCorner.vue";
import WelcomeText from "./components/WelcomeText.vue";
</script>

<template>
  <GithubCorner />
  <div class="layout">
    <WelcomeText />
    <div class="list">
      <ButtonCard text="About me"><InfoSVG class="icon" /></ButtonCard>
      <ButtonCard text="My works"><FolderOpenSVG class="icon" /></ButtonCard>
      <ButtonCard text="Github"><GithubSVG class="icon" /></ButtonCard>
      <ButtonCard text="Stay in touch">
        <span style="display: flex">
          <FacebookSquareSVG class="icon" />
          <LinkedinSquareSVG class="icon" />
        </span>
      </ButtonCard>
    </div>
  </div>
  <footer class="footer"></footer>
</template>

<style lang="scss">
.layout {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  margin: 50vh 20px 0 20px;
  gap: 2.5rem;
}

.list {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 2.5rem;
  width: 100%;
}

.footer {
  height: 10rem;
}

@media screen and (min-width: $mobile) {
  .layout {
    flex-direction: row;
    gap: 10vw;
    margin: auto;
  }
  .list {
    width: 30vw;
  }
  .footer {
    height: auto;
  }
}
</style>
