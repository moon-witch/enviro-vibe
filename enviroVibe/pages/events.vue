<script setup lang="ts">

const events = [
  {
    name: "Global Climate Strike",
    date: "21-07-2022",
    country: "USA",
    city: "New York",
    location: "Big Boulevard 12, 12345 New York",
    goal: "Raise awareness about climate change",
    RSVPneeded: false,
    currentRSVPs: 187,
    maxAttend: 500,
    imagePath: "/some/path/to/img1.png"
  },
  {
    name: "Sustainable Energy Conference",
    date: "15-08-2022",
    country: "UK",
    city: "London",
    location: "Hyde Park, W2 2UH London",
    goal: "Discuss renewable energy solutions",
    RSVPneeded: true,
    currentRSVPs: 450,
    maxAttend: 1000,
    imagePath: "/some/path/to/img2.png"
  },
  {
    name: "Eco-Friendly Tech Expo",
    date: "05-09-2022",
    country: "Germany",
    city: "Berlin",
    location: "Tech Street 22, 10115 Berlin",
    goal: "Showcase green technology innovations",
    RSVPneeded: true,
    currentRSVPs: 325,
    maxAttend: 600,
    imagePath: "/some/path/to/img3.png"
  },
  {
    name: "Plastic-Free Oceans Campaign",
    date: "12-10-2022",
    country: "France",
    city: "Paris",
    location: "Galleria Avenue 5, 75001 Paris",
    goal: "Promote ocean conservation and plastic reduction",
    RSVPneeded: false,
    currentRSVPs: 620,
    maxAttend: null,
    imagePath: "/some/path/to/img4.png"
  },
  {
    name: "Tree Planting Drive",
    date: "29-09-2022",
    country: "Canada",
    city: "Toronto",
    location: "Lakeside Park, M5V 3L9 Toronto",
    goal: "Plant trees to combat deforestation",
    RSVPneeded: true,
    currentRSVPs: 145,
    maxAttend: 400,
    imagePath: "/some/path/to/img5.png"
  },
  {
    name: "Zero-Waste Lifestyle Workshop",
    date: "03-11-2022",
    country: "USA",
    city: "San Francisco",
    location: "Silicon Valley Road, 94025 San Francisco",
    goal: "Teach people how to live a zero-waste life",
    RSVPneeded: true,
    currentRSVPs: 90,
    maxAttend: 350,
    imagePath: "/some/path/to/img6.png"
  },
  {
    name: "Sustainable Agriculture Summit",
    date: "25-10-2022",
    country: "India",
    city: "Mumbai",
    location: "Colaba Causeway, 400005 Mumbai",
    goal: "Explore sustainable farming practices",
    RSVPneeded: false,
    currentRSVPs: 300,
    maxAttend: 700,
    imagePath: "/some/path/to/img7.png"
  },
  {
    name: "Green Cities Initiative",
    date: "19-12-2022",
    country: "Italy",
    city: "Rome",
    location: "Piazza Navona, 00186 Rome",
    goal: "Promote sustainable urban planning",
    RSVPneeded: false,
    currentRSVPs: 800,
    maxAttend: null,
    imagePath: "/some/path/to/img8.png"
  },
  {
    name: "Clean Energy Film Screening",
    date: "10-01-2023",
    country: "Australia",
    city: "Sydney",
    location: "Cinema Street 18, 2000 Sydney",
    goal: "Showcase documentaries on clean energy",
    RSVPneeded: true,
    currentRSVPs: 150,
    maxAttend: 500,
    imagePath: "/some/path/to/img9.png"
  },
  {
    name: "Sustainability and Tech Meetup",
    date: "08-02-2023",
    country: "Japan",
    city: "Tokyo",
    location: "Shibuya Crossing, 150-0002 Tokyo",
    goal: "Network with sustainability and tech innovators",
    RSVPneeded: true,
    currentRSVPs: 270,
    maxAttend: 900,
    imagePath: "/some/path/to/img10.png"
  }
];


</script>

<template>
  <div class="event-container">
    <h1>Events</h1>
    <ul class="event-list">
      <li v-for="event of events">
        <EventWidget
            :name="event.name"
            :date="event.date"
            :country="event.country"
            :city="event.city"
            :location="event.location"
            :goal="event.goal"
            :max-attend="event.maxAttend"
            :RSVPneeded="event.RSVPneeded"
            :current-r-s-v-ps="event.currentRSVPs"
            :image-path="event.imagePath"
        />
      </li>
    </ul>
  </div>
</template>

<style scoped>
h1 {
  text-align: center;
}
</style>