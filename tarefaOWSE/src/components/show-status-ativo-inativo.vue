<template>
    <div>
        <span  :class="'badge ' + styleStatus" > {{tipoStatus}}</span>
    </div>
</template>

<script>
export default {
    props: {
        status: {
            type: String
        }
    },
    computed:{
        tipoStatus(){
            if(this.status == 'a'){
                return 'Ativo'
            }else if(this.status == 'i'){
                return 'Inativo'
            }else{
                return ''
            }
        },
        styleStatus(){
            if(this.status == 'a') {
                return 'badge-secondary'
            }else if( this.status =='i'){
                return 'badge-danger'
            }else{
                return ''
            }
        }
    }
}

</script>

<style scoped>

</style>