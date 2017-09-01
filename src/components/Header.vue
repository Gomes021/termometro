<template>
	<main class="container">
		<section class="container-opnioes">
	      <h1 class="opnioes-titulo"> COMO ESTÁ A AULA ?</h1>
	      <button class="imagens-icons" v-on:click="addOpniao('chata')">
	      	<img class="imagens-faces" src="../assets/faces/chata.svg">
	      	<p class="texto-img">CHATA</p>
	      </button>
	      <button class="imagens-icons" v-on:click="addOpniao('devagar')">
	      	<img class="imagens-faces" src="../assets/faces/devagar.svg">
	      	<p class="texto-img">DEVAGAR</p>
	      </button>
	      <button class="imagens-icons" v-on:click="addOpniao('ok')">
		     <img class="imagens-faces" src="../assets/faces/ok.svg">
		     <p class="texto-img">OK</p>
	      </button>
	      <button class="imagens-icons" v-on:click="addOpniao('animada')">
		     <img class="imagens-faces" src="../assets/faces/animada.svg">
		     <p class="texto-img">ANIMADA</p>
	      </button>
	      <button class="imagens-icons" v-on:click="addOpniao('incrivel')">
		     <img class="imagens-faces" src="../assets/faces/incrivel.svg">
		     <p class="texto-img">IN-CRÍ-VEL</p>
	      </button>
    	</section>
    	<section class="container-travado">
	      <div class="container-nome">
	    	<p class="meunome-texto">MEU NOME É</p>
	    	<input class="caixa-dialogo" type="text" v-on:keyup.enter ="addAluno()" v-model="nome">
	      </div>
	      <div class="container-trav">
	    	<button class="imagem-button" v-on:click="addAluno()">
	    	<img class="imagem-verm" src="../assets/imagens/button.png"></button>
	    	<p class="travado-texto">ESTOU TRAVADO !</p>
	      </div>	
	      <div class="alunos-travados">
	      	<ul class="alunostravados-lista" v-for="(aluno, index) in alunos">
	      		<li class="alunostravados-itens">
	      			<span>{{aluno.nome}}</span>
	      			<button v-on:click="deleteAluno(index)">x</button>
	      		</li>	      		
	      	</ul>
	      </div>
    	</section>
    	<section class="caixa-contador">
		   	<div class="imagens-icons">
		      	<img class="imagens-faces" src="../assets/faces/chata.svg">
		      	<p class="texto-img">CHATA</p>
		    </div>
		   	<div class="imagens-icons">
		      	<img class="imagens-faces" src="../assets/faces/devagar.svg">
		      	<p class="texto-img">DEVAGAR</p>
		    </div>
		    <div class="imagens-icons">
			     <img class="imagens-faces" src="../assets/faces/ok.svg">
			     <p class="texto-img">OK</p>
		    </div>
		    <div class="imagens-icons">
			     <img class="imagens-faces" src="../assets/faces/animada.svg">
			     <p class="texto-img">ANIMADA</p>
		    </div>
		    <div class="imagens-icons">
			     <img class="imagens-faces" src="../assets/faces/incrivel.svg">
			     <p class="texto-img">IN-CRÍ-VEL</p>
		      </div>
	    </section>
	</main>
</template>

<script>
	export default{
		name:'Header',
		data(){
			return{
				chata: 0,
				devagar: 0,
				ok: 0,
				animada: 0,
				incrivel: 0,
				opnioes: [{
					chata: 0,
					devagar: 0,
					ok: 0, 
					animada: 0,
					incrivel: 0
				}],

				nome:'',
				alunos: [{nome: 'ALUNOS TRAVADOS'}],
				
			}
		},
		methods:{
			addOpniao(opniao){
				console.log("addOpniao", opniao)
				this.opnioes[0][opniao] +=1
			},
			addAluno(){
				this.alunos.push({nome:this.nome})
			},
			deleteAluno(index){
				this.alunos.splice(index,1)
			},
		}

	}
	
</script>

<style scoped>
	.container{
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
	}
	.container-opnioes{
		display: flex;
		justify-content: center;
		align-items: center;
		flex-flow: row wrap;
		width: 100%;
	}
	.opnioes-titulo{
		font-family: 'Arial-black';
		font-weight: 900;
		font-style: normal;
		text-align: center;
		color: #FBAE16;
		width: 100%
	}
	.container-travado{
		width: 100%;
		min-height: 30vh;
		display: flex;
		justify-content: flex-start;
		align-items: center;
		margin-top: 25px;
	}

	.imagens-icons{
		width: 170px;
		height: 170px;
		margin: 4px;
		border-radius: 50%;
		border: solid #ccc 1px;
		background-color: #fff;
	}
	.imagens-faces{
		width: 70%;
	}
	.texto-img{
		font-family: 'Arial-black';
		font-weight: 900;
		font-style: normal;
		color: #0099FF;
		margin: auto;
	}
	.container-nome{
		display: flex;
		justify-content: flex-start;
		flex-direction: column;
		margin-top: 10%;
		margin-left: 10%;
		width: 18%;
	}
	.caixa-dialogo{
		border-radius: 30px 30px 30px 30px;
		height: 30px;
		border: solid #ccc 1px;
		text-align: center;
	}
	.meunome-texto{
		font-family: 'Arial-black';
		font-weight: 900;
		font-style: normal;
		display: flex;
		justify-content: flex-start;
		align-items: center;
		margin: 0;	
		color: #FBAE16;
	}
	.container-trav{
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		margin-left: 10%;
	}
	.imagem-button{
		background-color: transparent;
		border: none;
		width: 60%;
	}
	.imagem-verm{
		width: 100%;
	}
	.travado-texto{
		font-family: 'Arial-black';
		font-weight: 900;
		font-style: normal;
		color: #FBAE16;
	}
	.alunos-travados{
		padding: 15px;
		border: 1px solid #999;
		border-radius: 20px;
		min-width: 20%;
		min-height: 10vh;
		background-color: #fff;
	}
	.alunos-travados-lista{
		margin: 1px;
	}

	.alunos-travados-itens{
		
	}
	.caixa-contador{
		display: flex;
		justify-content: center;
		align-items: center;
		flex-flow: row wrap;
		width: 100%;
		background-color: #FFF;

	}
</style>
