<template>
  <div>
    <button @click="switchLayout">Switch layout to {{ nextLayout }}</button>
    <ul :class="layout === 'grid'? 'grid': 'list'">
      <li v-for="tweet in tweets" :key="tweet.id">
        <span><b>Tweeted by:</b> {{ tweet.user }} on <strong>{{ tweet.created_date }}</strong></span>
        <span>Tweet: {{ tweet.tweet }}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      layout: 'grid',
      nextLayout: 'list',
      tweets: [
        {
          id: 1,
          user: "John Doe",
          tweet: "Bacon ipsum dolor amet in brisket sunt, turducken shoulder biltong porchetta lorem shank ham hock laborum cow culpa quis. Frankfurter porchetta shoulder ham velit, burgdoggen et. Prosciutto pork chop commodo capicola duis tail, incididunt ribeye anim. Do strip steak ea, buffalo sunt salami jerky pork loin et eu occaecat elit incididunt biltong in",
          created_date: new Date()
        },
        {
          id: 2,
          user: "Anne Pearl",
          tweet: "Cupim do lorem sint, frankfurter commodo dolore chuck turducken doner fugiat tongue. Chislic do alcatra corned beef turkey. Cupim chislic turkey swine mollit et ea pork belly ground round tri-tip venison ut. Elit prosciutto aute porchetta sausage jerky. Ipsum venison filet mignon pork loin nulla duis adipisicing corned beef rump turducken sint short loin.",
          created_date: new Date()
        },
        {
          id: 3,
          user: "Herbert Parker",
          tweet: "Bacon ipsum dolor amet in brisket sunt, turducken shoulder biltong porchetta lorem shank ham hock laborum cow culpa quis. Frankfurter porchetta shoulder ham velit, burgdoggen et. Prosciutto pork chop commodo capicola duis tail, incididunt ribeye anim. Do strip steak ea, buffalo sunt salami jerky pork loin et eu occaecat elit incididunt biltong in",
          created_date: new Date()
        },
        {
          id: 4,
          user: "Net Ninja",
          tweet: "Landjaeger do chislic, occaecat sunt strip steak ham ground round bresaola flank meatloaf et fatback. Hamburger rump et, venison fugiat tail jerky. Laborum incididunt ut bacon qui, aliquip sed cillum do boudin doner proident commodo tongue swine. Proident excepteur picanha, ribeye alcatra culpa cillum meatloaf voluptate sirloin biltong ea adipisicing dolor t-bone",
          created_date: new Date()
        }
      ]
    }
  },
  methods: {
    switchLayout() {
      if (this.layout === 'grid') {
        this.layout = 'list'
        this.nextLayout = 'grid'
      } else {
        this.layout = 'grid'
        this.nextLayout = 'list'
      }
    }
  }
}
</script>

<style>
/* css for grid */
.grid {
	background-color: #ddedfb;
	list-style: none;
	margin: 0 auto;
	padding: 20px;
	text-align: left;
	width: 100%;
}
.grid li {
	display: inline-block;
	position: relative;
	width: 50%;
  margin-bottom: 5%;
}
.grid li:after {
	content: "";
	display: block;
	padding-bottom: 20%;
}
.grid li span {
	height: 99%;
	width: 98%;
}
/* end of css for grid */
/* css for list */
.list {
	background-color: #ddedfb;
	list-style: none;
	margin: 0 auto;
	padding: 0;
	text-align: left;
	width: 100%;
}

.list li {
	border-bottom: 1px solid #fff;
	overflow: hidden;
	padding: 20px;
	transition: background 0.2s linear;
}

.list li:hover {
	background-color: #fff;
}

button {
  margin-bottom: 2%;
}
</style>
