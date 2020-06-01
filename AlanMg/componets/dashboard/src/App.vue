<template>
  <div id= "app">
    <Navbar />
    <div class= "container-fluid">
      <div class= "row">
        <div class= "col-12">
          <p>Bar Chart</p>
        </div>
      </div>
      <div class= "row">
        <div class= "col-4">
          <Table :fiels="version_fields" :items="versions" :title="versions_title"/>
        </div>
        <div class= "col-4">
          <Table :items="devices" :title="device_title"/> 
        </div>
        <div class= "col-4">
          <Table :items="systems" :title="systems_title"/> 
        </div>
      </div>
      <div class= "row">
        <div class= "col-12">
          <Table :items="issues" :title="issues_title"/> 
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Table from "@/components/Table.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Table
  },
  data() {
    return {
      versions_title: "Crashes by Version",
      version_fields: [
          { key: 'version', sortable: false },
          { key: 'events', sortable: true },
          { key: 'users', sortable: false }
        ],
      versions: [
        { version: 2.64, events: '4,931', user: '4.013' },
        { version: 2.63, events: '3,999', user: '3,355' },
        { version: 2.62, events: '1,006', user: '970' }
      ],
      devices_title: "Crashes by Version",
      devices: [
        { "device model": "oneplus ",events: "3,596", user : "3,088"},
        { "device model": "mi A2", events: "2,797", user : "2,485" },
        { "device model": "Pixel XL", events: "1,961", user : "1,823" },
        { "device model": "Pixe 2", events: "1184", user : "1,119" },
        { "device model": "SM-G95", events: "398", user : "391" }
      ],
      systems_title: "Crashes by Version",
      systems: [
        { "operating system": "9", events: '3,548', user: '3,085' },
        { "operating system": "7.1.1", events: '2,783', user: '2,445' },
        { "operating system": "8.1.0", events: '2,004', user: '1,844' },
        { "operating system": "7.0", events: '1,156', user: '1,098' },
        { "operating system": "8.0.0", events: '426', user: '420' }
      ],
      issues_title: "Crashes by Version",
      issues: [
        { issue: "ProgressiveMode.java line 20", "Blam Frame": 'com.labpixies.flood.ProgressiveMode.getLevel', version: '2.64', events: "4,016", user: "2,287" },
        { issue: "ExtraStepsActivity.java line 145", "Blam Frame": 'com.labpixies.flood.ExtraStepsActivity.setUpPackage', version: '2.63', events: "3,900", user: "3,289" },
        { issue: "AdHelper.java line 150", "Blam Frame": 'com.labpixies.flood.AdHelper.populateAppInstallAdView', version: '2.64', events: "915", user: "882" },
        { issue: "ActivityThread.java line 2068", "Blam Frame": 'android.app.ActivityThread$H.handleMessage', version: '2.62', events: "791", user: "769" },
        { issue: "gr.java line 2", "Blam Frame": 'gr.run', version: '2.63', events: "215", user: "214" },
        { issue: "ks.java line 14", "Blam Frame": 'ks.a', version: '2.64', events: "99", user: "99" }
      ],
    }
  }
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto+Slab&display=swap');
#app {
  background-color: #F0F0F0;

}
</style>
