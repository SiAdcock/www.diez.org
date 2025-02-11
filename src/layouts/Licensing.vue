<template>
  <div class="page shared">
    <NavBar/>
    <section id="licensing" class="section section-narrow">
      <h2>Understanding Diez Licensing</h2>
      <p>Diez is Free and Open-Source Software, available for personal and commercial use, with <a href="https://github.com/diez/diez" target="_blank">source code available on GitHub</a>.</p>
      <p>Diez is published under a dual-license model in two editions: <strong>Community Edition</strong> and <strong>Enterprise Edition</strong>. Understanding these editions, their respective advantages, and the obligations/responsibilities that come with each edition is an important step to deciding how to adopt Diez within your project or organization.</p>

      <h3>Diez Community Edition</h3>
      <p><strong>Diez CE</strong> is licensed under the GPL family of licenses, specifically: the AGPL for most modules and LGPL for others.  This licensing maximizes flexibility for personal or commercial use, with a handful of notable exceptions.</p>
      <p>Diez CE licensing is ideal for use cases such as open source projects with open source distribution, student/academic purposes, hobby projects, internal research projects without external distribution, or other projects where all AGPL/LGPL obligations can be met.</p>
      <p>We chose these licenses carefully based on the licenses of commercially popular open-source developer tools like:</p>
      <ul>
        <li>GCC — the world’s most popular C / C++ compiler, GPL-licensed</li>
        <li>Git — the world’s most popular version-control command-line tool, GPL-licensed</li>
        <li>MongoDB — the world’s most popular NoSQL database server, formerly AGPL licensed, currently SSPL licensed</li>
        <li>The Qt Project — a cross-platform GUI-creation tool, GPL and LGPL licensed</li>
        <li>Neo4j — the world’s most popular graph database server, GPL licensed</li>
      </ul>

      <h4>AGPL modules: Compiler, Extractors, and CLI</h4>
      <p>In the same way that GCC and Git are widely used without restriction in commercial settings, Diez CE’s compiler, extractors, and CLI (licensed under the AGPL license) are all generally usable in the same way.  These pieces of Diez are all “compiler-like” or “command line interface-like” and are freely usable by individual developers at development time</p>
      <p>That said, if you modify any of the source code for these tools, dynamically or statically link them in any codebase (including via “shelling” or calling these tools via command-line from a codebase,) or otherwise distribute these tools as part of other codebases/systems, <strong>including via network access</strong> (for example in continuous integration (CI) servers, application (HTTP) servers, or automated build scripts) — <strong>be aware that you are obligated to open-source all related code & make publicly available under the AGPL license in turn.</strong></p>
      <p>If you are not willing or able to meet these requirements of the AGPL license, you will want Diez Enterprise Edition instead, which offers flexible commercial licensing. <a :href="typeformUrl" target="_blank">Contact us</a> for more info or if you have any questions about the obligations of the AGPL license.</p>

      <h4>LGPL module: Framework</h4>
      <p>Diez CE’s Framework module contains code intended to be dynamically linked inside your own proprietary codebases—i.e. it contains the code you import in order to create a Diez design language—so it’s licensed under the LGPL to ensure that it’s freely usable under most commercial use-cases.</p>
      <p>That said, <strong>“derivative works,” i.e. codebases using any modifications to the Diez Framework module itself, or any codebase that statically links Diez Framework code, must be open-sourced under LGPL and freely distributed in turn.</strong></p>
      <p>If you are not willing or able to meet these requirements of the LGPL license, you will want Diez Enterprise Edition instead, which offers flexible commercial licensing. <a :href="typeformUrl" target="_blank">Contact us</a> for more info or if you have any questions about the obligations of the LGPL license.</p>

      <h3>Diez Enterprise Edition</h3>
      <p><strong>Diez EE</strong> features three key advantages over Diez Community Edition:</p>
      <ul>
        <li>Flexible commercial licensing, free from the obligations of the GPL-family of licenses</li>
        <li>Enterprise-only add-ons, including Diez DocsGen</li>
        <li>Available support, integration, and training from the Diez team</li>
      </ul>
      <a :href="typeformUrl" target="_blank">Get in touch</a> to learn more about Diez EE.
    </section>
    <Footer/>
  </div>
</template>

<script>
import Footer from '@theme/components/Footer.vue';
import NavBar from '@theme/components/NavBar.vue';

export default {
  data () {
    return {
      typeformUrl: 'https://design-code.typeform.com/to/JnOi9o'
    };
  },
  components: {
    Footer,
    NavBar
  }
};
</script>

<style lang="scss" scoped>
  @import '@theme/styles/_utils.scss';

  h2 {
    margin-top: $sizing-xxs-px;
  }

  h3 {
    margin-top: $sizing-xxs-px;
  }

  p, li {
    line-height: 32px;
  }
</style>
