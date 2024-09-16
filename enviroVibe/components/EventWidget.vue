<script setup lang="ts">
const props = defineProps({
  name: String,
  date: String,
  country: String,
  city: String,
  location: String,
  goal: String,
  maxAttend: Number as PropType<number | null>,
  RSVPneeded: Boolean,
  currentRSVPs: Number,
  imagePath: String,
})
</script>

<template>
  <div class="event-widget">
    <div class="top-line">
      <div class="info">
        <div class="location">
          <div class="global">{{country}}, {{city}}</div>
          <div class="address">Location: {{location}}</div>
        </div>
        <div class="name">
          {{ name}}
        </div>
      </div>
      <div class="numbers">
        <div class="date">{{ date }}</div>
        <div v-if="maxAttend" class="max-attend">{{ maxAttend }} RSVP's max!</div>
        <div v-if="RSVPneeded" class="rsvp-need">RSVP only!</div>
      </div>
    </div>
    <div class="bot-line">
      <div class="image">
        Here will be an image
      </div>
      <div class="rsvp">
        <button class="rsvp-btn">RSVP</button>
        <p>{{currentRSVPs}} already RSVP'd</p>
      </div>
    </div>
  </div>
  </template>

<style scoped lang="scss">
.event-widget {
  border: 1px solid #2d642d;
  border-radius: 4px;
  padding: 1rem 2rem;
  width: 50rem;
  background: blanchedalmond;

  .top-line {
    display: flex;
    justify-content: space-between;
    gap: 3rem;

    .info {
      display: flex;
      flex-direction: column;
      gap: 1rem;

      .location {
        display: flex;
         gap: 2rem;
        align-items: center;

        .global {
          font-weight: bold;
          font-size: 1.2rem;
        }
      }
    }

    .numbers {
      text-align: end;
      .date {
        font-weight: bold;
        font-size: 1.2rem;
      }
    }

    .name {
      font-weight: bold;
      font-size: 1.5rem;
    }
  }

  .bot-line {
    margin-top: 1rem;
    display: flex;
    justify-content: space-between;

    .image {
      width: 200px;
      height: 120px;
      border: 1px solid #2d642d;
      border-radius: 4px;
      padding: 1rem;
    }

    .rsvp {
      display: flex;
      flex-direction: column;
      justify-content: end;

      .rsvp-btn {
        font-size: 1.2rem;
        font-weight: bold;
        background: #ceffce;
        border: 1px solid #2d642d;
        padding: .5rem 1rem;
        border-radius: 4px;
        cursor: pointer;
      }
    }
  }
}
</style>