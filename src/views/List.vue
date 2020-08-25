<template>
  <div>

    <input v-model="newContact" placeholder="Name" type="text" />
    <button @click="addContact">Add Contact</button>

    <transition-group name="slide-up" tag="ul" appear>
      <li v-for="(contact, index) in contacts" :key="index">
        {{ contact }}
      </li>
    </transition-group>

    <button @click="sortContacts">Sort</button>

  </div>
</template>

<script>
export default {
  data() {
    return {
      newContact: "",
      contacts: [
        "Beau Thabeast",
        "Cindy Rella",
        "Alice Wunderlind"
      ]
    }
  },
  methods: {
    addContact() {
      this.contacts.push(this.newContact)
      this.newContact = ""
    },
    sortContacts() {
      this.contacts = this.contacts.sort()
    }
  }
}
</script>