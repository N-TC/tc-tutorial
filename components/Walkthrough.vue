


<template>
  <div class="modal__background" @click.self="$emit('toggleWalkthrough')">
    <div class="modal__window walkthrough">
      <div v-for="i in [currentIndex]" :key='i'>
        <img :src="currentImg.url" />
      </div>

      <div v-if="currentIndex==0">
        <button class="prev" @click="$emit('toggleWalkthrough')">EXIT</button>
        <button class="next" @click="next" href='#'>START</button>
        <button class="modal__close" aria-label="Close Modal" @click="$emit('toggleWalkthrough')"/>
      </div>

      <div v-else-if="currentIndex==1">
        <button class="next next-tutorial1" @click="next" href='#'>NEXT</button>
        <button class="modal__close" aria-label="Close Modal" @click="$emit('toggleWalkthrough')"/>
      </div>

      <div v-else-if="currentIndex==2">
        <button class="next next-tutorial2" @click="next" href='#'>NEXT</button>
        <button class="modal__close" aria-label="Close Modal" @click="$emit('toggleWalkthrough')"/>
      </div>

      <div v-else-if="currentIndex==3">
        <button class="next next-tutorial3" @click="next" href='#'>NEXT</button>
        <button class="modal__close" aria-label="Close Modal" @click="$emit('toggleWalkthrough')"/>
      </div>

      <div v-else-if="currentIndex==4">
        <button class="next next-tutorial4" @click="next" href='#'>NEXT</button>
        <button class="modal__close" aria-label="Close Modal" @click="$emit('toggleWalkthrough')"/>
      </div>

      <div v-else-if="currentIndex==5">
        <button class="next next-tutorial5" @click="next" href='#'>NEXT</button>
        <button class="modal__close" aria-label="Close Modal" @click="$emit('toggleWalkthrough')"/>
      </div>

      <div v-else-if="currentIndex==6">
        <button class="next next-tutorial6" @click="next" href='#'>NEXT</button>
        <button class="modal__close" aria-label="Close Modal" @click="$emit('toggleWalkthrough')"/>
      </div>

      <div v-else-if="currentIndex==7">
        <button class="next next-tutorial7" @click="next" href='#'>NEXT</button>
        <button class="modal__close" aria-label="Close Modal" @click="$emit('toggleWalkthrough')"/>
      </div>

      <div v-else-if="currentIndex==8">
        <button class="next next-tutorial8" @click="next" href='#'>NEXT</button>
        <button class="modal__close" aria-label="Close Modal" @click="$emit('toggleWalkthrough')"/>
      </div>

      <div v-else-if="currentIndex==9">
        <button class="next next-tutorial9" @click="next" href='#'>NEXT</button>
        <button class="modal__close" aria-label="Close Modal" @click="$emit('toggleWalkthrough')"/>
      </div>

      <div v-else-if="currentIndex==10">
        <button class="next next-tutorial10" @click="next" href='#'>NEXT</button>
        <button class="modal__close" aria-label="Close Modal" @click="$emit('toggleWalkthrough')"/>
      </div>

      <div v-else-if="currentIndex==11">
        <button class="next next-tutorial11" @click="next" href='#'>NEXT</button>
        <button class="modal__close" aria-label="Close Modal" @click="$emit('toggleWalkthrough')"/>
      </div>

      <div v-else>
        <button class="next tutorialLast" aria-label="Close Modal" @click="$emit('toggleWalkthrough')">DONE</button>
      </div>
      
  </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      images:[
        { url: 'images/lcl-tutorial1.png'},
        { url: 'images/lcl-tutorial2.png'},
        { url: 'images/lcl-tutorial3.png'}, 
        { url: 'images/lcl-tutorial4.png'},
        { url: 'images/lcl-tutorial5.png'},
        { url: 'images/lcl-tutorial6.png'},
        { url: 'images/lcl-tutorial7.png'},
        { url: 'images/lcl-tutorial8.png'}, 
        { url: 'images/lcl-tutorial9.png'},
        { url: 'images/lcl-tutorial10.png'},
        { url: 'images/lcl-tutorial11.png'},
        { url: 'images/lcl-tutorial12.png'},
        { url: 'images/lcl-tutorial13.png'},
      ],
      currentIndex: 0
    }
  },
  
    methods: {
      next() {
        this.currentIndex += 1
      },
      prev() {
        this.currentIndex -= 1
      }
    },
  
    computed: {
      currentImg() {
        return this.images[Math.abs(this.currentIndex) % this.images.length];
      }
    }
}
</script>

<style lang="scss" scoped>
.walkthrough {
  background: rgb(39, 33, 33);
  border: 2px solid rgba(0, 0, 0, 0.5);
  opacity: 1.0;
  color: $white;
  border-radius:10px;
}

img {
height:600px;
width:100%
  }
.prev, .next {
  cursor: pointer;
  text-align: center;
  background: red; 
  position: absolute;
  top: 40%;
  // width: 93px;
  width: 22%;
  padding: 10px;
  color: white;
  font-weight: bold;
  font-size: 18px;
  border-radius: 4px 4px 4px 4px;
  text-decoration: none;
  user-select: none;
}

.next {
  right: 19%;
  top: 59.3%;
}

.prev {
  left:19%;
  top: 59.3%;
}

.next-tutorial1 {
  right: 39%;
  top: 33%;
}

.next-tutorial2 {
  left: 18%;
  top: 36.2%;
}

.next-tutorial3 {
  left: 40%;
  top: 28%;
}

.next-tutorial4 {
  left: 41%;
  top: 35.5%;
}

.next-tutorial5 {
  left: 43%;
  top: 27.3%;
}

.next-tutorial6 {
  left: 43%;
  top: 27.3%;
}

.next-tutorial7 {
  left: 41%;
  top: 51.2%;
}

.next-tutorial8 {
  right: 33%;
  top: 44.2%;
}

.next-tutorial9 {
  left: 39%;
  top: 48.5%;
}

.next-tutorial10 {
  left: 52%;
  top: 47.5%;
}

.next-tutorial11 {
  left: 39%;
  top: 55.5%;
}

.tutorialLast {
  left: 39%;
  top: 58.8%;
}

.prev:hover, .next:hover {
  background-color: rgba(255,0,0,0.9);
}

.close {
  background: url('/icons/x.svg') no-repeat 50%;
    background-size: 13px 13px;
    transform: rotate(45deg);
    position: absolute;
    width: 24px;
    height: 24px;
    padding: 4px;
    // top: -10px;
    // right: -10px;
    // top: 12px;
    // right: 12px;
    background-color: $dark-orange;
    border-radius: 50%;
    color: $white;
    display: flex;
    align-items: center;
    justify-content: center;
    }

//   .tutorial{
//     top: 12px;
//     right: 12px;
// }

// .close-tutorial7 {
//     top: 49px;
//     right: 21px;
// }

// .close-tutorial8 {
//     top: 49px;
//     right: 21px;
// }

// .close-tutorial9 {
//     top: 49px;
//     right: 21px;
// }
</style>
