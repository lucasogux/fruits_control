<template>
  <main>
    <section class="p-10 bg-[#E5E5E5] rounded-lg">
      <div class="container mx-auto">
        <!--criação-->
        <div class="flex lg:flex-wrap">
          <div class="lg:w-6/12 w-full lg:pr-5">
            <div class="bg-[#D1DBFF] rounded-lg flex flex-col lg:items-start items-center p-6 w-full h-full gap-4">
              <h2 class="font-bold text-xl mb-1">Criar balde</h2>
              <div class="flex flex-col lg:items-start items-center gap-2 w-full" id="capacidade">
                <p>Capacidade</p>
                <input type="text" class="rounded-lg border-none px-4 py-2 w-full" placeholder="Digite aqui">
              </div>
              <button class="bg-[#3763FF] hover:bg-indigo-600 w-full text-white py-2 px-4 rounded-lg" onclick="cadastrarBalde()">Salvar</button>
            </div>
          </div>
          <div class="lg:w-6/12 w-full lg:pr-5">
            <div class="bg-[#D1DBFF] rounded-lg flex flex-col lg:items-start items-center p-6 w-full h-full gap-4">
              <h2 class="font-bold text-xl mb-1">Criar fruta</h2>
              <div class="flex flex-col lg:items-start items-center gap-2 w-full" id="frutaA">
                <p>Nome</p>
                <input type="text" class="rounded-lg border-none px-4 py-2 w-full" placeholder="Digite aqui">
              </div>
              <div class="flex flex-col lg:items-start items-center gap-2 w-full" id="frutaB">
                <p>Nome</p>
                <input type="text" class="rounded-lg border-none px-4 py-2 w-full" placeholder="Digite aqui">
              </div>
              <button class="bg-[#3763FF] hover:bg-indigo-600 w-full text-white py-2 px-4 rounded-lg" onclick="cadastrarBalde()">Salvar</button>
            </div>
          </div>
        </div>
        <!--listagem-->
        <div class="flex gap-4">
          <div class="w-max bg-[#3763FF] rounded-lg text-white flex py-4 px-6 items-center my-6">
            <div class="pr-6 border-r border-white">
              <h2 class="text-lg font-bold">Fruta B</h2>
              <p>R$ 3.90</p>
            </div>
            <div class="pl-6">
              <button class="hover:scale-110" id="FruitDropdown1" data-dropdown-toggle="dropdown2">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
                  aria-hidden="true">
                  <path
                    d="M19 3H5C3.89543 3 3 3.89543 3 5V19C3 20.1046 3.89543 21 5 21H19C20.1046 21 21 20.1046 21 19V5C21 3.89543 20.1046 3 19 3Z"
                    stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M12 8V16" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M8 12H16" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                </svg>
              </button>
            </div>
          </div>
          <div class="w-max bg-[#3763FF] rounded-lg text-white flex py-4 px-6 items-center my-6">
            <div class="pr-6 border-r border-white">
              <h2 class="text-lg font-bold">Fruta A</h2>
              <p>R$ 3.90</p>
            </div>
            <div class="pl-6">
              <button class="hover:scale-110" id="FruitDropdown2" data-dropdown-toggle="dropdown2">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
                  aria-hidden="true">
                  <path
                    d="M19 3H5C3.89543 3 3 3.89543 3 5V19C3 20.1046 3.89543 21 5 21H19C20.1046 21 21 20.1046 21 19V5C21 3.89543 20.1046 3 19 3Z"
                    stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M12 8V16" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M8 12H16" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                </svg>
              </button>
            </div>
          </div>
          <!-- Dropdown menu -->
          <div id="dropdown2"
            class="z-50 hidden bg-white divide-y divide-gray-100 rounded-lg shadow w-max dark:bg-gray-700">
            <div class="grid grid-cols-2 p-6 gap-3">
              <button class="rounded-lg hover:bg-gray-300 bg-[#E5E5E5] py-3 px-5">Balde 1</button>
              <button class="rounded-lg hover:bg-gray-300 bg-[#E5E5E5] py-3 px-5">Balde 2</button>
              <button class="rounded-lg hover:bg-gray-300 bg-[#E5E5E5] py-3 px-5">Balde 3</button>
              <button class="rounded-lg hover:bg-gray-300 bg-[#E5E5E5] py-3 px-5">Balde 4</button>
            </div>
          </div>
        </div>
        <!--total-->
        <div class="bg-[#D1DBFF] rounded-lg w-full lg:pr-5">
          <div class="rounded-lg flex flex-col lg:items-start items-center p-6 w-full h-full gap-4">
            <div class="bg-[#3763FF]  p-4 text-white w-max rounded-lg">
              <div class="flex gap-4">
                <h2 class="text-lg">Total: 8.45</h2>
                <button class="hover:scale-110">
                  <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M3 6H5H21" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                    <path
                      d="M8 6V4C8 3.46957 8.21071 2.96086 8.58579 2.58579C8.96086 2.21071 9.46957 2 10 2H14C14.5304 2 15.0391 2.21071 15.4142 2.58579C15.7893 2.96086 16 3.46957 16 4V6M19 6V20C19 20.5304 18.7893 21.0391 18.4142 21.4142C18.0391 21.7893 17.5304 22 17 22H7C6.46957 22 5.96086 21.7893 5.58579 21.4142C5.21071 21.0391 5 20.5304 5 20V6H19Z"
                      stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                    <path d="M10 11V17" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                    <path d="M14 11V17" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  </svg>
                </button>
              </div>
              <div class="flex flex-col gap-2 mt-4">
                <div class="bg-white rounded-lg flex flex-col items-center justify-center text-gray-900 py-2 px-4">
                  <h2 class="text-lg font-bold">Fruta B</h2>
                  <p>R$ 4.55</p>
                </div>
                <div class="bg-white rounded-lg flex flex-col items-center justify-center text-gray-900 py-2 px-4">
                  <h2 class="text-lg font-bold">Fruta A</h2>
                  <p>R$ 5.55</p>
                </div>
              </div>
            </div>
          </div>
          <div class="lg:ml-auto mx-auto px-6 pb-6">
            Capacidade: 50%
          </div>
        </div>
      </div>
    </section>
  </main>
</template>


<script>
class Balde {
    constructor(capacidade, frutaA, frutaB) {
        this.capacidade = capacidade;
        this.frutaA = frutaA;
        this.frutaB = frutaB;
    }
}

class Bd {
    constructor() {
        let id = localStorage.getItem('id');

        if (id === null) {
            localStorage.setItem('id', 0);
        }
    }

    getProximoId() {
        let getProximoId = localStorage.getItem('id');
        return parseInt(getProximoId) + 1;
    }

    gravar(d) {
        let id = this.getProximoId();
        localStorage.setItem(id, JSON.stringify(d));
        localStorage.setItem('id', id);
    }
}

let bd = new Bd();

function cadastrarBalde() {
    let capacidade = document.getElementById('capacidade').value;
    let frutaA = document.getElementById('frutaA').value;
    let frutaB = document.getElementById('frutaB').value;

    let balde = new Balde(capacidade, frutaA, frutaB);

    bd.gravar(balde);
}

</script>

<script setup>
import { onMounted } from 'vue'
import { initFlowbite } from 'flowbite'
onMounted(() => {
  initFlowbite();
})
</script>

