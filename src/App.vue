<template>
  <div class="periodic-table">
    <Element v-for="element in elements"
             v-bind:key="element"
             :atomicNumber="element.atomicNumber"
             :symbol="element.symbol"
             :name="element.name"
             :atomicMass="element.atomicMass"/>
  </div>
</template>

<script>
import Element from './components/Element.vue'

export default {
  name: 'App',
  components: {
    Element
  },
  data(){
    return{
      elements: [
        //Row 1
        {isEmpty: false, atomicNumber: 1, symbol: "H", name: "Hydrogen", atomicMass: 1.008},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: false, atomicNumber: 2, symbol: "He", name: "Helium", atomicMass: 4.0026},
        

        //Row 2
        {isEmpty: false, atomicNumber: 3, symbol: "Li", name: "Lithium", atomicMass: 6.941},
        {isEmpty: false, atomicNumber: 4, symbol: "Be", name: "Beryllium", atomicMass: 9.0122},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: false, atomicNumber: 5, symbol: "B", name: "Boron", atomicMass: 10.811},
        {isEmpty: false, atomicNumber: 6, symbol: "C", name: "Carbon", atomicMass: 12.011},
        {isEmpty: false, atomicNumber: 7, symbol: "N", name: "Nitrogen", atomicMass: 14.007},
        {isEmpty: false, atomicNumber: 8, symbol: "O", name: "Oxygen", atomicMass: 15.999},
        {isEmpty: false, atomicNumber: 9, symbol: "F", name: "Fluorine", atomicMass: 18.998},
        {isEmpty: false, atomicNumber: 10, symbol: "Ne", name: "Neon", atomicMass: 20.180},

        //Row 3
        {isEmpty: false, atomicNumber: 11, symbol: "Na", name: "Sodium", atomicMass: 22.990},
        {isEmpty: false, atomicNumber: 12, symbol: "Mg", name: "Magnesium", atomicMass: 24.305},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: false, atomicNumber: 13, symbol: "Al", name: "Aluminum", atomicMass: 26.982},
        {isEmpty: false, atomicNumber: 14, symbol: "Si", name: "Silicon", atomicMass: 28.086},
        {isEmpty: false, atomicNumber: 15, symbol: "P", name: "Phosporus", atomicMass: 30.974},
        {isEmpty: false, atomicNumber: 16, symbol: "S", name: "Sulfur", atomicMass: 32.065},
        {isEmpty: false, atomicNumber: 17, symbol: "Cl", name: "Fluorine", atomicMass: 35.453},
        {isEmpty: false, atomicNumber: 18, symbol: "Ar", name: "Argon", atomicMass: 39.948},

        //Row 4
        {isEmpty: false, atomicNumber: 19, symbol: "K", name: "Potassium", atomicMass: 39.098},
        {isEmpty: false, atomicNumber: 20, symbol: "Ca", name: "Calcium", atomicMass: 40.078},
        {isEmpty: false, atomicNumber: 21, symbol: "Sc", name: "Scandium", atomicMass: 44.956},
        {isEmpty: false, atomicNumber: 22, symbol: "Ti", name: "Titanium", atomicMass: 47.867},
        {isEmpty: false, atomicNumber: 23, symbol: "V", name: "Vanadium", atomicMass: 50.942},
        {isEmpty: false, atomicNumber: 24, symbol: "Cr", name: "Chromium", atomicMass: 51.996},
        {isEmpty: false, atomicNumber: 25, symbol: "Mn", name: "Manganese", atomicMass: 54.938},
        {isEmpty: false, atomicNumber: 26, symbol: "Fe", name: "Iron", atomicMass: 55.845},
        {isEmpty: false, atomicNumber: 27, symbol: "Co", name: "Cobalt", atomicMass: 58.933},
        {isEmpty: false, atomicNumber: 28, symbol: "Ni", name: "Nickel", atomicMass: 58.693},
        {isEmpty: false, atomicNumber: 29, symbol: "Cu", name: "Copper", atomicMass: 63.546},
        {isEmpty: false, atomicNumber: 30, symbol: "Zn", name: "Zinc", atomicMass: 65.39},
        {isEmpty: false, atomicNumber: 31, symbol: "Ga", name: "Gallium", atomicMass: 69.723},
        {isEmpty: false, atomicNumber: 32, symbol: "Ge", name: "Germanium", atomicMass: 71.61},
        {isEmpty: false, atomicNumber: 33, symbol: "As", name: "Arsenic", atomicMass: 74.922},
        {isEmpty: false, atomicNumber: 34, symbol: "Se", name: "Selenium", atomicMass: 78.96},
        {isEmpty: false, atomicNumber: 35, symbol: "Br", name: "Bromine", atomicMass: 79.904},
        {isEmpty: false, atomicNumber: 36, symbol: "Kr", name: "Krypton", atomicMass: 83.80},

        //Row 5
        {isEmpty: false, atomicNumber: 37, symbol: "Rb", name: "Rubidium", atomicMass: 85.468},
        {isEmpty: false, atomicNumber: 38, symbol: "Sr", name: "Strontium", atomicMass: 87.62},
        {isEmpty: false, atomicNumber: 39, symbol: "Y", name: "Yttrium", atomicMass: 88.906},
        {isEmpty: false, atomicNumber: 40, symbol: "Zr", name: "Zirconium", atomicMass: 91.224},
        {isEmpty: false, atomicNumber: 41, symbol: "Nb", name: "Niobium", atomicMass: 92.906},
        {isEmpty: false, atomicNumber: 42, symbol: "Mo", name: "Molybdenum", atomicMass: 95.94},
        {isEmpty: false, atomicNumber: 43, symbol: "Tc", name: "Technetium", atomicMass: "[98]"},
        {isEmpty: false, atomicNumber: 44, symbol: "Ru", name: "Ruthenium", atomicMass: 101.07},
        {isEmpty: false, atomicNumber: 45, symbol: "Rh", name: "Rhodium", atomicMass: 102.91},
        {isEmpty: false, atomicNumber: 46, symbol: "Pd", name: "Palladium", atomicMass: 106.42},
        {isEmpty: false, atomicNumber: 47, symbol: "Ag", name: "Silver", atomicMass: 107.87},
        {isEmpty: false, atomicNumber: 48, symbol: "Cd", name: "Cadmium", atomicMass: 112.41},
        {isEmpty: false, atomicNumber: 49, symbol: "In", name: "Indium", atomicMass: 114.82},
        {isEmpty: false, atomicNumber: 50, symbol: "Sn", name: "Tin", atomicMass: 118.71},
        {isEmpty: false, atomicNumber: 51, symbol: "Sb", name: "Antimony", atomicMass: 121.76},
        {isEmpty: false, atomicNumber: 52, symbol: "Te", name: "Tellurium", atomicMass: 127.60},
        {isEmpty: false, atomicNumber: 53, symbol: "I", name: "Iodine", atomicMass: 126.90},
        {isEmpty: false, atomicNumber: 54, symbol: "Xe", name: "Xenon", atomicMass: 131.29},

        //Row 6
        {isEmpty: false, atomicNumber: 55, symbol: "Cs", name: "Cesium", atomicMass: 132.905},
        {isEmpty: false, atomicNumber: 56, symbol: "Ba", name: "Barium", atomicMass: 4.003},
        {isEmpty: false, atomicNumber: 71, symbol: "Lu", name: "Lutetium", atomicMass: "[262]"},
        {isEmpty: false, atomicNumber: 72, symbol: "Hf", name: "Hafnium", atomicMass: 178.49},
        {isEmpty: false, atomicNumber: 73, symbol: "Ta", name: "Tantalum", atomicMass: 180.95},
        {isEmpty: false, atomicNumber: 74, symbol: "W", name: "Tungsten", atomicMass: 183.84},
        {isEmpty: false, atomicNumber: 75, symbol: "Re", name: "Rhenium", atomicMass: 186.21},
        {isEmpty: false, atomicNumber: 76, symbol: "Os", name: "Osmium", atomicMass: 190.23},
        {isEmpty: false, atomicNumber: 77, symbol: "Ir", name: "Iridium", atomicMass: 192.22},
        {isEmpty: false, atomicNumber: 78, symbol: "Pt", name: "Platinum", atomicMass: 195.08},
        {isEmpty: false, atomicNumber: 79, symbol: "Au", name: "Gold", atomicMass: 196.97},
        {isEmpty: false, atomicNumber: 80, symbol: "Hg", name: "Mercury", atomicMass: 200.59},
        {isEmpty: false, atomicNumber: 81, symbol: "Tl", name: "Thallium", atomicMass: 204.38},
        {isEmpty: false, atomicNumber: 82, symbol: "Pb", name: "Lead", atomicMass: 207.2},
        {isEmpty: false, atomicNumber: 83, symbol: "Bi", name: "Bismuth", atomicMass: 208.98},
        {isEmpty: false, atomicNumber: 84, symbol: "Po", name: "Polonium", atomicMass: "[209]"},
        {isEmpty: false, atomicNumber: 85, symbol: "At", name: "Astatine", atomicMass: "[210]"},
        {isEmpty: false, atomicNumber: 86, symbol: "Rn", name: "Radon", atomicMass: "[222]"},

        //Row 7 TODO
        {isEmpty: false, atomicNumber: 87, symbol: "Fr", name: "Francium", atomicMass: 223.020},
        {isEmpty: false, atomicNumber: 88, symbol: "Ra", name: "Radium", atomicMass: 6.941},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},

        //Row 8
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: true},

        //Row 9 TODO
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: true},
        {isEmpty: true},

        //Row 10 TODO
        {isEmpty: true},
        {isEmpty: true},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: false, atomicNumber: 1, symbol: "Symb", name: "Name", atomicMass: 0.001},
        {isEmpty: true},
        {isEmpty: true},
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  position: fixed;
  top: 0px;
  left: 0px;
  width: 100vw;
  height: 100vw;
  background-color: rgb(219, 219, 219);
  color: #2c3e50;
}
.periodic-table{
  display: grid;
  grid-template-columns: repeat(18, 90px);
  position: relative;
  left: 50px;
  top: 50px;
}
</style>
