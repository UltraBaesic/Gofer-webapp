<template>
  <main id="post-errand">
    <div class="min-map">
      <div class="map-progress">
        <div>
          <p class="map">Category</p>
          <p class="circle-filled"></p>
          <p class="progress-line"></p>
        </div>
        <div class="sub-map">
          <p class="map">Location</p>
          <p class="circle-empty"></p>
          <p class="progress-line"></p>
        </div>
        <div class="sub-map">
          <p class="map">&nbsp; &nbsp; Details</p>
          <p class="circle-empty"></p>
          <p class="progress-line"></p>
        </div>
        <div class="sub-map">
          <p class="map">&nbsp; Preview</p>
          <p class="circle-empty"></p>
        </div>
      </div>
      <h4 class="bold-title text-left mt-3">What kind of Errand do you want to run?</h4>
    </div>
                        <div class="card-items">
                        <p class="card-item"><i class="material-icons md-24">local_mall</i>&nbsp; Shopping
                        </p>
                        <p class="card-item"><i class="material-icons md-24">local_shipping</i>&nbsp; Pick
                            up &
                            Delivery</p>
                        <p class="card-item"><i class="material-icons md-24">fastfood</i>&nbsp; Catering
                            Service</p>
                        <p class="card-item"><i class="material-icons md-24">ac_unit</i>&nbsp;
                            Cleaning</p>
                        <p class="card-item"><i class="material-icons md-24">local_laundry_service</i>&nbsp;
                            Laundry</p>
                        <p class="card-item"><i class="material-icons md-24">school</i>&nbsp; Reading/Writing</p>
                        <p class="card-item"><i class="material-icons md-24">style</i>&nbsp; Ticketing</p>
                        <p class="card-item"><i class="material-icons md-24">home_work</i>&nbsp; Real Estate
                        </p>
                        <p class="card-item"><i class="material-icons md-24">school</i>&nbsp; Tutoring</p>
                        <p class="card-item"><i class="material-icons md-24">home_work</i>&nbsp; Chauffer
                        </p>
                        <p class="card-item"><i class="material-icons md-24">toys</i>&nbsp; Gardening
                        </p>
                        <p class="card-item"><i class="material-icons md-24">room_service</i>&nbsp; Food
                            Purchase</p>
                        <p class="card-item"><i class="material-icons md-24">devices_other</i>&nbsp;
                            Electronics
                            Repair</p>
                        <p class="card-item"><i class="material-icons md-24">phone_iphone</i>&nbsp; Phones
                            Repair</p>
                        <p class="card-item"><i class="material-icons md-24">laptop</i>&nbsp; Computers
                            Repair</p>
                        <p class="card-item"><i class="material-icons md-24">local_shipping</i>&nbsp; Moving
                        </p>
                        <p class="card-item"><i class="material-icons md-24">child_friendly</i>&nbsp; Baby
                            Sitting</p>
                        <p class="card-item"><i class="material-icons md-24">weekend</i>&nbsp; Carpentry
                        </p>
                        <p class="card-item card-item-2"><i class="material-icons md-24">school</i>&nbsp; Research &
                            Documentation</p>
                        <p class="card-item"><i class="material-icons md-24">directions_car</i>&nbsp; Auto
                            Repairs</p>
                        <p class="card-item card-item-2"><i class="material-icons md-24">home_work</i>&nbsp; Fashion and
                            Tailoring</p>
                        <p class="card-item"><i class="material-icons md-24">motorcycle</i>&nbsp; Errands
                        </p>
                        <p class="card-item"><i class="material-icons md-24">home_work</i>&nbsp; Make Up
                            Artistry</p>
                        <p class="card-item"><i class="material-icons md-24 text-dark">view_carousel</i>&nbsp;
                            Others
                        </p>
                    </div>
  </main>
</template>

<script>
export default {
  data(){
    return {
      data: undefined
    }
  },
  methods: {
    
  }
}

</script>

<style scoped>
@import url(https://fonts.googleapis.com/icon?family=Material+Icons);

#post-errand {
  color: #333333;
}

.map-progress {
  display: flex;
}

.map {
  font-size: 18px;
  font-weight: bold;
}

.sub-map {
  margin-left: -3rem;
}

.circle-filled {
  width: 1.5rem;
  height: 1.5rem;
  background-color: lightgray;
  border: 7px solid #0086b9;
  border-radius: 50%;
  display: inline-block;
  margin-left: 2rem;
}

.circle-empty {
  width: 1.5rem;
  height: 1.5rem;
  background-color: #eef6f9;
  border: 5px solid lightgray;
  border-radius: 50%;
  display: inline-block;
  margin-left: 2rem;
  z-index: 3;
}

.progress-line {
  min-width: 150px;
  border-bottom: 2px solid lightgray;
  margin-bottom: 26px;
  /* margin-left: -5px; */
  display: inline-block;
  z-index: 0;
}

.progress-line-filled {
  min-width: 150px;
  border-bottom: 2px solid #0086b9;
  margin-bottom: 26px;
  margin-left: -5px;
  display: inline-block;
  z-index: 0;
}
.min-map {
  margin: 1rem;
}

.card-item {
    display: inline-block;
    background: transparent;
    padding: 0.7em 1.5em;
    margin: 0.7em 0.5em;
    font-weight: bold;
    border-radius: 10px;
    box-shadow: 4px 4px 8px rgba(81, 81, 81, 0.26), -3px -3px 6px rgba(209, 233, 242, 0.44) !important;
    cursor: pointer;
    width: 220px;
}

.card-item:hover {
    box-shadow: 1px 1px 6px 1px rgba(0, 0, 0, 0.3) !important;
    color: white;
    transition: all 0.2s ease-in-out;
    background-color: #0086b9;
}
.material-icons {
    vertical-align: middle;
    margin-top: -2px;
    color: #999999;
}

.card-item:hover .material-icons {
    color: white;
}

.card-item-2 {
    width: calc(440px + 1.25em) !important;
}
</style>