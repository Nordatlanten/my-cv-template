<template>
  <aside class="cv-aside">
    <h2>Contact</h2>
    <ul class="contact-list">
      <li>
        <img src="../assets/mail_icon.svg" alt="Email Icon">
        <a>{{ email ? email : "email@email.org" }}</a>
      </li>
      <li>
        <img src="../assets/github_icon.svg" alt="Github Icon">
        <a :href="githubUrl ? githubUrl : 'https://www.example.com/'">
          {{ githubName ? githubName : "Github username" }}
        </a>
      </li>
      <li>
        <img src="../assets/phone_icon.svg" alt="Phone Icon" />
        <span>{{ phoneNumber ? phoneNumber : "+00 123 - 456789" }}</span>
      </li>
    </ul>
    <h2>Skills</h2>
    <ul class="skills-list">
      <li>Lorem / IpSum / Dolor</li>
      <li>Sit / Amet / Consectetur / Adipisicing</li>
      <li>Elit / Vel / Quibusdam Veritatis</li>
      <li>Veritatis Amet / Corporis At & Possimus </li>
      <li>Aperiam / Et / Suscipit (first lorem)</li>
    </ul>
    <h2>past projects</h2>
    <ul class="past-projects-list">
      <li><a>https://lorem.se</a></li>
      <li><a>https://ipsumdolorsit.se</a></li>
      <li><a>https://consectetur.se/adipisicing</a></li>
      <li><a>https://elit-vel.com.et</a></li>
    </ul>
    <CVPeekhole />
  </aside>
</template>

<script setup lang="ts">
import CVPeekhole from './CVPeekhole.vue';

defineProps<{ email?: string, githubName?: string, githubUrl?: string, phoneNumber?: string }>()
</script>

<style lang="scss" scoped>
.cv-aside {
  max-width: 23vw;

  ul {
    padding: 0;
    margin: 0;
    display: flex;
    flex-direction: column;
    gap: 2mm;
    margin-bottom: 0.8cm;
    font-size: 0.9rem;

    li {
      display: flex;
      align-items: center;
      gap: 2mm;
      font-family: Shibui-Light, serif;
      letter-spacing: 0.2mm;

      a,
      a:visited {
        text-decoration: none;
        color: unset;
        cursor: pointer;
      }

      a:hover {
        filter: invert(0.5);
      }

      img {
        max-width: 22px;
      }
    }
  }

  ul.skills-list {
    list-style-type: circle;
    gap: 1mm;
  }

  ul.past-projects-list {
    gap: 0.3mm;
  }
}
</style>
