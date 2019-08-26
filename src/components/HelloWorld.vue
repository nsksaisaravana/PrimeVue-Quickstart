<template>
  <div>
    <h3 class="first">Basic</h3>
    <DataTable :value="cars">
        <Column field="vin" header="Vin"></Column>
        <Column field="year" header="Year"></Column>
        <Column field="brand" header="Brand"></Column>
        <Column field="color" header="Color"></Column>
    </DataTable>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class HelloWorld extends Vue {
  //@Prop() private msg!: string;
  
  
  //private columns=[];
  @Prop()
    public cars: any;



  public mounted() {
      this.cars = {
          data: [
              {brand: 'Volkswagen', year: 2012, color: 'Orange', vin: 'dsad231ff'},
          ],
      };
  }


}
</script>
