<template>
 <q-page class="q-pa-md">
   <q-card>
     <q-card-section>
       <div class="text-h6">Formulário de Cadastro</div>
     </q-card-section>
     <q-card-section>
       <q-form>
         <div class="row q-col-gutter-md">
           <div class="col-12 col-md-6 col-sm-12">
             <q-input outlined stack-label label="Nome Completo *" v-model="dados.nome_completo" />
           </div>
           <div class="col-12 col-md-6 col-sm-12">
             <q-input outlined stack-label label="E-mail *" v-model="dados.email" />
           </div>
           <div class="col-12 col-md-6 col-sm-12">
             <q-input outlined stack-label label="Telefone *" v-model="dados.telefone" />
           </div>
           <div class="col-12 col-md-6 col-sm-12">
             <q-select
               outlined
               stack-label
               label="Sexo *"
               :options="options"
               v-model="dados.sexo"
             />
           </div>
         </div>

         <div class="q-mt-md">
           <q-btn
             label="Enviar"
             type="submit"
             color="primary"
             @click="enviar(dados)"
           />
           <q-btn
             label="Cancelar"
             type="reset"
             color="primary"
             flat
             class="q-ml-sm"
           />
         </div>
       </q-form>
     </q-card-section>
   </q-card>
 </q-page>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'PageIndex',
 data() {
   return {
     dados: {},
     options: ['Masculino' , 'Feminino', 'Outros'],
   };
 },
 methods: {
   enviar(dados) {
     console.log(dados)
   },
 },
});
</script>
