<template>
  <section class="hours px-4 py-5">
    <div class="p-3 p-lg-5 pt-lg-3">
      <div class="row mb-2">
        <div class="col-md-6">
          <div class="row g-0 border rounded overflow-hidden flex-md-row mb-4 shadow-sm h-md-250 position-relative">
            <h1 class="display-4 fw-bold lh-1 py-2">Hours of Operation</h1>
            <div 
              class="lead row"
              v-for="operation in operations"
              v-bind:operation="operation"
              v-bind:key="operation.day"
              >
              <div class="col">
                <p>
                  {{ operation.day.capitalize() }}
                </p>
              </div>
              <div class="col">
                <p>
                  {{ operation.hours }}
                </p>
              </div>
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <div class="row g-0 border rounded overflow-hidden flex-md-row mb-4 shadow-sm h-md-250 position-relative">
            <h1 class="display-4 fw-bold lh-1 py-2">
              Prices
            </h1>
            <div 
              class="lead row"
              v-for="price in prices"
              v-bind:price="price"
              v-bind:key="price.type"
              >
              <div class="col">
                <p>
                  {{ price.type }}
                </p>
              </div>
              <div class="col">
                <p>
                  {{ price.value }}
                </p>
              </div>
            </div>
            <p>
              American Crew and Sukesha products are available at discount prices.
            </p>
            <hr/>
            <p>
              Special offer! $3 off your first visit,
              just mention this offer.
              (expires Nov. 30)
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
String.prototype.capitalize = function() {
    return this.charAt(0).toUpperCase() + this.slice(1);
}

export default {
  name: 'Hours',
  components: {
  },
  data: function () {
    return {
      operations: [
        {day: "monday", hours: "9:00am - 7:00pm"},
        {day: "tuesday", hours: "9:00am - 7:00pm"},
        {day: "wednesday", hours: "9:00am - 7:00pm"},
        {day: "thursday", hours: "9:00am - 8:00pm"},
        {day: "friday", hours: "9:00am - 8:00pm"},
        {day: "saturday", hours: "9:00am - 5:00pm"},
        {day: "sunday", hours: "Closed"},
      ],
      prices: [
        {type: "Men", value: "$21"}, 
        {type: "Women", value: "$25+"}, 
        {type: "Seniors", value: "$19"}, 
        {type: "Children 12 and under", value: "$19"}, 
        ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hours {
  background-color: #F8FCFB;
}

.title {
  padding: 5px;
}
</style>
