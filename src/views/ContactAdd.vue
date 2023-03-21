<template>
  <div v-if="contact" class="page">
    <h4>Thêm mới Liên hệ</h4>
    <contact-form :contact="contact" @submit:contact="createContact" />
    <p>{{ message }}</p>
  </div>
</template>

<script>
import ContactForm from "@/components/ContactForm.vue";
import ContactService from "@/services/contact.service";

export default {
  components: {
    ContactForm,
  },

  data() {
    return {
      contact: {},
      message: "",
    };
  },
  methods: {
    createContact(data) {
      try {
        ContactService.create(data);
        this.message = "Liên hệ được thêm thành công.";
      } catch (error) {
        console.log(error);
      }
    },
  },
};
</script>