<template>
    <div class="content" style="width: 40%;">
        <div class="row mb-3">
            <div class="col-md-2 text-right col-xs-12 text-xs-left">
                <label class="control-label obrigatorio" for="camada">Camada:</label>
            </div>
            <div class="col-md-4 col-xs-12">
                <select class="form-select" name="camada" id="camada">
                    <option value="0" selected="selected">Selecione...</option>
                    <option v-for="option in camadasOption" :key="option.value" :value="option.value">{{ option.name }}</option>
                </select>
            </div>
            <div class="col-md-2 text-right col-xs-12 text-xs-left">
                <label class="control-label obrigatorio" for="atributo">Atributo:</label>
            </div>
            <div class="col-md-4 col-xs-12">
                <select class="form-select" name="atributo" id="atributo">
                    <option value="0" selected="selected">Selecione...</option>
                    <option v-for="option in atributosOption" :key="option.value" :value="option.value">{{ option.name }}</option>
                </select>
            </div>
        </div>
        <div class="row mb-3">
            <div class="col-md-2 text-right col-xs-12 text-xs-left">
                <label class="control-label obrigatorio" for="operador">Operador:</label>
            </div>
            <div class="col-md-4 col-xs-12">
                <select class="form-select" name="operador" id="operador">
                    <option value="0" selected="selected">Selecione...</option>
					<option value="EQUAL">== (Igual)</option>
                    <option value="NOT_EQUAL">!= (Diferente)</option>
                    <option value="LESS">&lt; (Menor)</option><option value="GREATER">&gt; (Maior)</option>
                    <option value="LESS_EQUAL">&lt;= (Menor ou igual)</option>
                    <option value="GEATER_EQUAL">&gt;= (Maior ou igual)</option>
                    <option value="BETWEEN">.. (Entre)</option>
                    <option value="LIKE">~ (Similar)</option>
                </select>
            </div>
            <div class="col-md-2 text-right col-xs-12 text-xs-left">
                <label for="valor" class="obrigatorio">Valor:</label>
            </div>
            <div class="col-md-4 col-xs-12">
                <input type="text" class="form-control" name="valor" id="valor" maxlength="30">
                <small id="valor1" class="form-text text-muted">Máximo de caracteres: 30</small>
            </div>
        </div>
        <div class="row barra-de-acoes">
            <div class="form-group" style="margin-top: 8px;">
                <button type="submit" class="btn btn-primary">Buscar</button>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';
    export default defineComponent ({
        name: 'FiltroBusca',
        inject: ['camadasOption', 'atributosOption']
    })

    
</script>

<style>
.form-select{
    border-radius: 0;
}

.text-right{
    text-align: right!important;
}   
</style>