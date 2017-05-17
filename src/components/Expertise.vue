<template>
<div class="">
  <div class="tile is-ancestor">
    <div class="tile is-parent">
      <div class="tile is-child">
        <jmob-card :image="cards[0].image"
                   :title="cards[0].title"
                   :anchor-name="cards[0].anchorName"
                   :lazy-time="cards[0].lazyTime"
                   :content="cards[0].content"></jmob-card>
      </div>
    </div>
    <div class="tile is-parent">
      <div class="tile is-child">
        <jmob-card :image="cards[1].image"
                   :title="cards[1].title"
                   :anchor-name="cards[1].anchorName"
                   :lazy-time="cards[1].lazyTime"
                   :content="cards[1].content"></jmob-card>
      </div>
    </div>
  </div>
  <div class="tile is-ancestor">
    <div class="tile is-parent">
      <div class="tile is-child">
        <jmob-card :image="cards[2].image"
                   :title="cards[2].title"
                   :anchor-name="cards[2].anchorName"
                   :lazy-time="cards[2].lazyTime"
                   :content="cards[2].content"></jmob-card>
      </div>
    </div>
    <div class="tile is-parent">
      <div class="tile is-child">
        <jmob-card :image="cards[3].image"
                   :title="cards[3].title"
                   :anchor-name="cards[3].anchorName"
                   :lazy-time="cards[3].lazyTime"
                   :content="cards[3].content"></jmob-card>
      </div>
    </div>
    <div class="tile is-parent">
      <div class="tile is-child">
        <jmob-card :image="cards[4].image"
                   :title="cards[4].title"
                   :anchor-name="cards[4].anchorName"
                   :lazy-time="cards[4].lazyTime"
                   :content="cards[4].content"></jmob-card>
      </div>
    </div>
  </div>
</div>



  <!-- <jmob-card :image="card.image"
             :title="card.title"
             :anchor-name="card.anchorName"
             :lazy-time="card.lazyTime"
             :content="card.content"></jmob-card> -->

</template>

<script>
import JmobCard from './Card.vue'
export default {
  data () {
    return {
      cards: [
        {
          image: '../static/images/fita.jpg',
          anchorName: 'atelie',
          lazyTime: 150,
          title: 'Ateliê de Software',
          content: `<p>Seja para um smartphone, tablet ou browser, desenvolvemos soluções baseadas na junção das melhores ferramentas e metodologias de
                   desenvolvimento de software. Nosso objetivo é atender as demandas, criando <strong>produtos digitais flexíveis e escaláveis</strong>, oferecendo
                   autonomia e independência para sua empresa. </p>
                   <p>Nossos projetos de softwares são conduzidos em parceria e num relacionamento transparente.
                   Adotamos uma <strong>metodologia ágil</strong>, onde a definição de escopo é constantemente validada e com <strong>entregas fracionadas</strong>.
                   Um formato que acreditamos ser um modelo mais efetivo para garantir tão logo o <strong>retorno do investimento</strong>.</p>`
        },
        {
          image: '../static/images/js.svg',
          anchorName: 'javascript',
          lazyTime: 300,
          title: 'Javascript',
          content: `<p>Somos especialistas em tecnologias baseadas no <strong>javascript</strong>, tanto no frontend como no backend.</p>
                    <p>Sempre que possível, adotamos o javascript a fim de uniformizar e simplificar o desenvolvimento.
                    O javascript é poderoso a ponto de deixar sua aplicação acessível, com codificação clara e fácil de <strong>escalar</strong>.</p>
                    <p>Embora nosso foco seja o javascript, também atuamos com expertise em outras tecnologias. </p>`
        },
        {
          image: '../static/images/tela.jpg',
          anchorName: 'knowhow',
          lazyTime: 350,
          title: 'Front-end',
          content: `<ul>
                      <li>Javascript / Ecmascript 6+</li>
                      <li>Vue.js</li>
                      <li>HTML / CSS</li>
                      <li>Bulma CSS</li>
                      <li>Material Design</li>
                      <li>Metodologia Flexbox</li>
                      <li>Sites Responsivos</li>
                      <li>SPA - Single Page Application</li>
                      <li>Quasar Framework</li>
                      <li>AngularJS</li>
                      <li>Ionic Framework</li>
                    </ul>
                    </ul>`
        },
        {
          image: '../static/images/motor2.jpg',
          anchorName: 'knowhow',
          lazyTime: 350,
          title: 'Back-end',
          content: `<ul>
                      <li>Node.js</li>
                      <li>Express</li>
                      <li>PHP / Laravel</li>
                      <li>Restful API</li>
                      <li>MongoDB</li>
                      <li>Mysql</li>
                      <li>Oracle</li>
                      <li>Postgresql</li>
                    </ul>`
        },
        {
          image: '../static/images/cubo.jpg',
          anchorName: 'atuacao',
          lazyTime: 450,
          title: 'Atuação',
          content: `<ul>
            <li>Consultoria para startups</li>
            <li>Aplicações mobile</li>
            <li>Aplicações web</li>
            <li>Progressive web apps</li>
            <li>Sites</li>
            <li>Blogs</li>
            <li>Landing pages</li>
          </ul>`
        }
      ]
    }
  },
  components: {
    JmobCard
  }
}
</script>

<style lang="css">
</style>
