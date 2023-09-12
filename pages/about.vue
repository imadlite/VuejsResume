<template>
  <div>
    <MobileLayout>
      <img :src="TopImage" class="w-full h-28 rounded-xl object-cover" />
      <div class="flex flex-col gap-6 lg:gap-9 mx-auto w-full md:w-10/12">
        <SectionParagraph>
          I'm Imad Djeddai, an Algeria-based Full Stack mobile developer
          specializing in Flutter, Laravel, and Node.js. I'm a graduate with a
          master's degree in Computer Science from Arbi Tebessi University, with
          an insatiable passion for learning new technologies. My expertise lies
          in crafting robust mobile applications using Flutter for the frontend
          and Laravel and Node.js for the backend. I'm dedicated to harnessing
          the power of these technologies to create seamless and visually
          appealing mobile interfaces that enhance the user experience.
        </SectionParagraph>
        <SectionParagraph>
          I'm currently working full-time for
          <LinkBtn link="https://www.trileotech.com" text="Trileotech" />
          , a leading mobile development company. I'm also working on iOS Apps
          like
          <LinkBtn
            link="https://github.com/mightykillrr/hanako"
            text="Hanako"
          />
          to assist me with various tasks on my Discord Server. Additionally,
          I'm constantly learning about GraphQL and UI/UX. Before this, I used
          to create various Node.js mobile apps/programs to fulfill my needs,
          which greatly enhanced my web development skills.
        </SectionParagraph>
        <SectionParagraph>
          My journey into Mobile development began during high school when I was
          introduced to Dart and Flutter. I quickly started building simple Apps
          with Flutter with State Mangement. After 1 Year, I delved deeper into
          Mobile development and explored various frameworks. Among them, I fell
          in love with Flutter, and I've been mastering it ever since. With each
          new project, I've added new tools to my skillset, such as GetX,
          Provider, Maps, and more.
        </SectionParagraph>
        <SectionParagraph>
          You can find my projects on my
          <LinkBtn link="https://github.com/mightykillrr" text="GitHub" />
          or on my
          <LinkBtn link="/" text="Portfolio" />
          page. I don't update my portfolio page frequently, but you can find
          all my recent projects on GitHub.
        </SectionParagraph>
        <SectionParagraph>
          Outside of work, I enjoy playing Valorant and CS:GO, listening to
          music on Spotify, or simply hanging out on Discord with friends. You
          can follow my life updates on
          <LinkBtn
            link="https://www.instagram.com/aniketkotal/"
            text="Instagram"
          />
          or
          <LinkBtn link="https://twitter.com/mightykillrr" text="Twitter" />
          . I don't post very often, so you may not find many posts on either
          platform.
        </SectionParagraph>
        <SectionParagraph>
          Credits to
          <LinkBtn link="https://www.pexels.com/@readymade" text="@readymade" />
          for the header picture!
        </SectionParagraph>
      </div>
      <hr class="bg-squgily bg-repeat border-0 h-[6px] opacity-25 my-6" />
      <div class="flex flex-col gap-5">
        <SectionTitle>Work</SectionTitle>
        <MobileLayout name="section">
          <WorkListItem v-for="work in works" :key="work.id" :work="work" />
        </MobileLayout>
      </div>
    </MobileLayout>
  </div>
</template>

<script setup>
import { useWorkStore } from '../store/workStore';
import TopImage from '../assets/imgs/about-image.jpg';

const workStore = useWorkStore();
const works = workStore.getAllWorks;
</script>
