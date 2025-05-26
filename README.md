# 🚀 Alura 100% Ultra Turbo Max Premium Ultra Fast v3

Um **bookmarklet** poderoso para automatizar tarefas da plataforma Alura — incluindo vídeos, exercícios de múltipla escolha, blocos interativos e envio de links de projeto. Tudo com apenas um clique!

> ⚠️ Uso destinado a fins **educacionais e de automação pessoal**.  
> Não nos responsabilizamos pelo uso indevido desta ferramenta.

---

## 📦 Funcionalidades

- ✅ Inicia vídeos automaticamente.
- ✅ Responde automaticamente exercícios com alternativas corretas visíveis no HTML.
- ✅ Embaralha e envia blocos de código.
- ✅ Gera um link aleatório do GitHub e envia no campo de projeto.
- ✅ Avança para a próxima tarefa automaticamente.
- ✅ Exibe uma mensagem secreta no centro da tela.

---

## 🛠 Como usar

1. **Copie o código do bookmarklet** abaixo.
2. Crie um **novo favorito (bookmark)** no seu navegador.
3. No campo de URL, cole o código (deve começar com `javascript:`).
4. Acesse uma atividade na Alura com URL do tipo:
5. Clique no favorito e o script executará automaticamente.

---

## 🔗 Bookmarklet

```javascript
javascript:(function(){function e(){console.log("🎯 Executando solveTask..."),t();const e=document.querySelector(".vjs-big-play-button");e&&(e.click(),console.log("▶️ Vídeo iniciado!"));document.querySelectorAll('li[data-correct="true"] input[type="checkbox"]:not(:checked)').forEach(e=>e.click()),document.querySelectorAll('.alternativeList-item[data-correct="true"] input[type="radio"]:not(:checked)').forEach(e=>e.click());const c=document.querySelector(".blocks");if(c){const e=Array.from(c.querySelectorAll(".block"));if(e.length>0){!function(e){for(let t=e.length-1;t>0;t--){const c=Math.floor(Math.random()*(t+1));[e[t],e[c]]=[e[c],e[t]]}}(e),e.forEach(e=>e.click());const t=document.getElementById("submitBlocks");t&&(t.click(),console.log("📦 Blocos enviados!"))}}const o=document.querySelector('input[name="linkUrl"]'),n=document.querySelector('button[type="submit"]');if(o&&n&&""===o.value.trim()){const e=`https://github.com/${Math.random().toString(36).substring(2,10)}`;o.value=e,console.log("🔗 Link gerado:",e),n.click(),console.log("✅ Link enviado!")}const r=document.querySelector(".task-actions-button-next");r&&(r.click(),console.log("⏭️ Próxima atividade!"))}function t(){const e=document.createElement("div");e.textContent=decodeURIComponent(escape(window.atob("QnkgQWRyaWVsIERldg=="))),Object.assign(e.style,{position:"fixed",top:"50%",left:"50%",transform:"translate(-50%, -50%)",padding:"15px 30px",backgroundColor:"#000",color:"#fff",borderRadius:"12px",fontSize:"20px",fontWeight:"bold",zIndex:1e4,opacity:.8,pointerEvents:"none",boxShadow:"0 0 20px rgba(0,0,0,0.7)"}),document.body.appendChild(e)}console.log("🚀 Alura Ultra Turbo Max Premium Ultra Fast ativado!"),setTimeout(e,1e3)})();
