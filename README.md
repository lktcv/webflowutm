# Webflow UTM
Configurando UTMs no Webflow 

Esse código tem como função colocar um parametro dentro do botão para o time de marketing rastraer o click.



## Como aplicar no seu website
1. Vá até a sua página e clique nas configurações.
2. Dentro do BODY você coloco esse código.
3. Trocar todas as url que estão escrito meusite.com.br para a sua url.
```
<script>
document.getElementById('botaoevento').onclick = function redirecionarComCupom() {
  const urlParams = new URLSearchParams(window.location.search);

  if (!urlParams.has('cupom')) {
    const finalUrl = https://www.meusite.com.br{urlParams.toString()};
    window.location.href = finalUrl;
  }
}

// Adicione eventos de clique para cada botão com ID 'botaoevento' de 1 a 8
for (let i = 1; i <= 8; i++) {
  const botao = document.getElementById(botaoevento${i});
  if (botao) {
    botao.addEventListener('click', function() {
      const urlParams = new URLSearchParams(window.location.search);

      if (!urlParams.has('cupom')) {
        const finalUrl = https://www.meusite.com.br{urlParams.toString()};
        window.location.href = finalUrl;
      }
    });
  }
}
</script>
```
4. Depois adiciona esse código e Troque a URL para o seu site.
```
<script>
  document.addEventListener('DOMContentLoaded', function() {
    const urlParams = new URLSearchParams(window.location.search);

    for (let i = 1; i <= 8; i++) {
      const botao = document.getElementById(botaoevento${i});
      if (botao) {
        botao.addEventListener('click', function(event) {
          const finalUrl = https://www.meusite.com.br{urlParams.toString()};

          // Impede o comportamento padrão de clicar no link
          event.preventDefault();

          // Abre a nova página manualmente
          window.open(finalUrl, '_self');
        });
      }
    }
  });
</script>
```
5. Para finalizar coloque o ID em todos os botões que você quer rastrear.
6. E Pode publicar.
