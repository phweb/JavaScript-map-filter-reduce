<template>
  <div class="hello">
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


<p>O <b>Filter</b> cria um novo array com todos os elementos que passaram no teste ad função fornecida</p>

<!-- HTML generated using hilite.me --><div style="background: #272822; overflow:auto;width:auto;border:solid gray;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #66d9ef">var</span> <span style="color: #a6e22e">newArray</span> <span style="color: #f92672">=</span> <span style="color: #a6e22e">arr</span><span style="color: #f8f8f2">.</span><span style="color: #a6e22e">filter</span><span style="color: #f8f8f2">(</span><span style="color: #a6e22e">callback</span><span style="color: #f8f8f2">[,</span> <span style="color: #a6e22e">thisArg</span><span style="color: #f8f8f2">])</span>
</pre></div>

<p> Vamos descobrir quais clientes são menor de idade com a função <b>filter:</b></p>
<p>Resultado</p>
  <div class="result">
{{menorIdade}}
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

</style>
