<template>
  <div class="content">
    <img alt="Vue logo" src="../assets/logo.png">
    <h1>{{ msg }}</h1>
<br/>
<p>Temos um array de objeto com clientes de varias idades</p>
<!-- HTML generated using hilite.me --><div style="background: #272822; overflow:auto;width:auto;border:solid gray;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #a6e22e">clientes</span><span style="color: #f92672">:</span> <span style="color: #f8f8f2">[{</span>
        <span style="color: #a6e22e">nome</span><span style="color: #f92672">:</span> <span style="color: #e6db74">&quot;Paulo&quot;</span><span style="color: #f8f8f2">,</span>
        <span style="color: #a6e22e">idade</span><span style="color: #f92672">:</span> <span style="color: #ae81ff">33</span><span style="color: #f8f8f2">,</span>
      <span style="color: #f8f8f2">},</span>
      <span style="color: #f8f8f2">{</span>
        <span style="color: #a6e22e">nome</span><span style="color: #f92672">:</span> <span style="color: #e6db74">&quot;Fernando&quot;</span><span style="color: #f8f8f2">,</span>
        <span style="color: #a6e22e">idade</span><span style="color: #f92672">:</span> <span style="color: #ae81ff">13</span><span style="color: #f8f8f2">,</span>
      <span style="color: #f8f8f2">},</span>
      <span style="color: #f8f8f2">{</span>
        <span style="color: #a6e22e">nome</span><span style="color: #f92672">:</span> <span style="color: #e6db74">&quot;Lucas&quot;</span><span style="color: #f8f8f2">,</span>
        <span style="color: #a6e22e">idade</span><span style="color: #f92672">:</span> <span style="color: #ae81ff">22</span><span style="color: #f8f8f2">,</span>
      <span style="color: #f8f8f2">},</span>
      <span style="color: #f8f8f2">{</span>
        <span style="color: #a6e22e">nome</span><span style="color: #f92672">:</span> <span style="color: #e6db74">&quot;Maria&quot;</span><span style="color: #f8f8f2">,</span>
        <span style="color: #a6e22e">idade</span><span style="color: #f92672">:</span> <span style="color: #ae81ff">9</span><span style="color: #f8f8f2">,</span>
      <span style="color: #f8f8f2">}]</span>
</pre></div>


<p>O <b>Filter</b> Cria um novo array com todos os elementos que passaram no teste da função fornecida</p>

<!-- HTML generated using hilite.me --><div style="background: #272822; overflow:auto;width:auto;border:solid gray;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #66d9ef">var</span> <span style="color: #a6e22e">newArray</span> <span style="color: #f92672">=</span> <span style="color: #a6e22e">arr</span><span style="color: #f8f8f2">.</span><span style="color: #a6e22e">filter</span><span style="color: #f8f8f2">(</span><span style="color: #a6e22e">callback</span><span style="color: #f8f8f2">[,</span> <span style="color: #a6e22e">thisArg</span><span style="color: #f8f8f2">])</span>
</pre></div>

<p> Vamos descobrir quais clientes são menor de idade com a função <b>filter:</b></p>
<p>Resultado do Filter</p>
{{menorIdade}}
<p>O <b>Map</b> Chama o callback para cada elemento e devolve um novo array com a mesma quantidade de items</p>
<!-- HTML generated using hilite.me --><div style="background: #272822; overflow:auto;width:auto;border:solid gray;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #66d9ef">var</span> <span style="color: #a6e22e">newArray</span> <span style="color: #f92672">=</span> <span style="color: #a6e22e">arr</span><span style="color: #f8f8f2">.</span><span style="color: #a6e22e">map</span><span style="color: #f8f8f2">(</span><span style="color: #a6e22e">callback</span><span style="color: #f8f8f2">[,</span> <span style="color: #a6e22e">thisArg</span><span style="color: #f8f8f2">])</span>
</pre></div>
<p>Vamos listar os nomes de todos os clientes com a função <b>Map:</b> </p>
<p>Resultado do Map</p>
{{nomeCliente}}
<p>O <b>Reduce</b> Executa uma função para cada elemento retornando um único valor de retorno</p>
 
<!-- HTML generated using hilite.me --><div style="background: #272822; overflow:auto;width:auto;border:solid gray;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #66d9ef">const</span> <span style="color: #a6e22e">reducer</span> <span style="color: #f92672">=</span> <span style="color: #f8f8f2">(</span><span style="color: #a6e22e">accumulator</span><span style="color: #f8f8f2">,</span> <span style="color: #a6e22e">currentValue</span><span style="color: #f8f8f2">)</span> <span style="color: #f92672">=&gt;</span> <span style="color: #a6e22e">accumulator</span> <span style="color: #f92672">+</span> <span style="color: #a6e22e">currentValue</span><span style="color: #f8f8f2">;</span>
</pre></div>
{{totalIdade}}


  <div class="result">
 
  </div>



  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      clientes: [{
        nome: "Paulo",
        idade: 33,
      },
      {
        nome: "Fernando",
        idade: 13,
      },
      {
        nome: "Lucas",
        idade: 22,
      },
      {
        nome: "Maria",
        idade: 9,
      }]
    }
  },
  computed:{
    menorIdade(){
      const deMenor = this.clientes.filter((cliente) => {
        return cliente.idade < 18
      })
      return deMenor;
    },
    nomeCliente(){
            const nome = this.clientes.map((cliente) => {
        return cliente.nome
      })
      return nome;
    },
    totalIdade(){
      const total = this.clientes.reduce((soma, totalCliente) => {
        return soma + totalCliente.idade
      }, 0)
      return "Soma total de todas as idade: " + total;
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.result {
  margin-bottom: 150px;
}
.content{
margin: 0 auto;
padding: 150px
}
</style>
