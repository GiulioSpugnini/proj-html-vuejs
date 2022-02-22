<template>
  <section class="bg-gray">
      <div class="container">
        <div class="row text-center justify-content-center">
          <div class="col-12">
            <h1 class="purple">Contact Us</h1>
            <p class="text-secondary">Our postal address and contact details</p>
            <img class="py-4" src="../assets/img/header_divider.png" alt="" />
          </div>
          <div v-for="(contact, index) in contacts" :key="index" class="col-3">
            <img :src="contact.icon" />
            <h4 class="purple py-3">{{ contact.name }}</h4>
            <h6 class="text-secondary">{{ contact.firstInfo }}</h6>
            <h6 class="text-secondary">{{ contact.secondInfo }}</h6>
            <h6 class="text-secondary">{{ contact.thirdInfo }}</h6>
          </div>
          <div class="col-6">
            <input type="text" placeholder="Your Name *" class="form-control my-4" />
            <input type="email" placeholder="Your E-mail *" class="form-control my-4" />
            <input type="text" placeholder="Subject" class="form-control my-4" />
          </div>
          <div class="col-6">
            <div class="mb-3">
              <textarea
                class="form-control my-4 textarea"
                placeholder="Your Message *"
                id="exampleFormControlTextarea1"
                rows="3"
              ></textarea>
            </div>
          </div>
          <button class="bg-orange text-white border-0">SEND MESSAGE</button>
        </div>
      </div>
  </section>
</template>

<script>
export default {
  name: "Contacts",
  data() {
    return {
      contacts: [
        {
          icon: require("../assets/img/envelope (1).png"),
          name: "Postal Address",
          firstInfo: "Fable Care Center",
          secondInfo: "85 Fentiman Ave",
          thirdInfo: "Ottawa, ON K1S 0T7",
        },
        {
          icon: require("../assets/img/mobile.png"),
          name: "Postal Address",
          firstInfo: "Phone: 1-800-64-38",
          secondInfo: "Fax: 1-800-64-39",
          thirdInfo: "office@fable.com",
        },
        {
          icon: require("../assets/img/clock.png"),
          name: "Postal Address",
          firstInfo: "Monday-Friday",
          secondInfo: "8.00 am - 5.00 pm",
          thirdInfo: "Weekend Closed",
        },
        {
          icon: require("../assets/img/document (1).png"),
          name: "Postal Address",
          firstInfo: "Mornings, 8 am - 12 noon",
          secondInfo: "Afternoons, 1 pm - 5 pm",
          thirdInfo: "Full Day, 8 am - 5 pm",
        },
      ],
    };
  },
};
</script>

<style scoped>
section{
    padding-top: 100px;
    padding-bottom: 100px;
}
.textarea{
    min-height: 160px;
}
button {
  width: 150px;
  padding: 10px;
}
</style>