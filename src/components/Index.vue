<template>
  <q-layout>
    <div slot="header" class="toolbar">
      <q-toolbar-title :padding="1">
        Quasar Vue Demo App
      </q-toolbar-title>
    </div>

    <q-tabs slot="navigation" class="justified" :refs="$refs" default-tab="tab-1">
      <q-tab name="tab-1" icon="message">
        Data Grid
      </q-tab>
      <q-tab name="tab-2" icon="message">
        Table
      </q-tab>
      <!-- q-tab name="tab-2" disable icon="fingerprint">
        Tab 2
      </q-tab>
      <q-tab name="tab-3" icon="alarm">
        Tab 3
      </q-tab>
      <q-tab name="tab-4" icon="accessibility">
        Tab 4
      </q-tab>
      <q-tab name="tab-5" hidden icon="accessibility">
        Tab 5
      </q-tab -->  
    </q-tabs>

    <!--
      Replace following "div" with
      "<router-view class="layout-view">" component
      if using subRoutes
    -->
    <div class="layout-view">
      <div class="layout-padding">
        <!-- Targets -->
        <div ref="tab-1">
          <q-data-table
            :data="table"
            :config="config"
            :columns="columns"
          >
          </q-data-table>
        </div>
        <div ref="tab-2">
          <table class="q-table cell-delimiter loose ">
            <tbody>
              <tr>
                <td data-th="name">Jawaid</td>
                <td data-th="age">32</td>
              </tr>
              <tr>
                <td data-th="name">Salman</td>
                <td data-th="age">30</td>
              </tr>
              <tr>
                <td data-th="name">Noman</td>
                <td data-th="age">31</td>
              </tr>
            </tbody>
          </table>
        </div>
        <!--<div ref="tab-3">
          <p>This is tab 3</p>
        </div>
        <div ref="tab-4">
          <p>This is tab 4</p>
        </div>
        <div ref="tab-5">
          <p>This is tab 5</p>
        </div>    -->
      </div>
    </div>
  </q-layout>
</template>
<script>
// import Quasar, { Utils } from 'quasar'

export default {
  data () {
    return {
      config: {
        // [REQUIRED] Set the row height
        rowHeight: '50px'
      },
      columns: [
        {
          // [REQUIRED] Column name
          label: '',
          // [REQUIRED] Row property name
          field: 'name',
          // [REQUIRED] Column width
          width: '100px'
        },
        {
          // [REQUIRED] Column name
          label: '',
          // [REQUIRED] Row property name
          field: 'isodate',
          // [REQUIRED] Column width
          width: '100px'
        }
      ],
      table: [
        {
          name: 'Jawaid',
          isodate: '4 Jan 2017'
        },
        {
          name: 'Michael',
          isodate: '5 Jan 2017'
        }
      ]
    }
  }
}

</script>

<style lang="styl">
</style>
