---
name: identidade-visual
description: Identidade visual única do AgenteFácil (paleta, contraste e regras de uso das cores). Carregue SEMPRE que for criar ou alterar qualquer coisa visual - tela, componente, página, site, banner, e-mail, imagem, ícone ou arte. Define as cores permitidas, a cor dos botões e a regra de nunca indicar estado só por cor.
---

# Identidade visual da Convert IA (projeto AgenteFácil)

Esta é a identidade visual única da Convert IA (projeto AgenteFácil). Use-a em tudo o que for criado ou alterado de agora em diante. Não peça ao proprietário para repeti-la.

O robô (ícone do AgenteFácil) é a origem das cores. A paleta abaixo foi tirada dele. Esta skill não inclui imagens.

## Contexto importante

O proprietário é daltônico. Por isso as regras de contraste e de "nunca só cor" abaixo são obrigatórias, não preferência estética.

## Paleta

Sempre escreva o nome e o código juntos (por exemplo, "Azul-marinho profundo #152542"), para o proprietário conseguir conferir sem depender de ver a cor.

| Nome | Código | Uso |
|---|---|---|
| Azul-marinho profundo | #152542 | Texto e títulos |
| Azul-marinho médio | #1F314E | Superfícies escuras |
| Azul-acinzentado escuro | #2E3F58 | Apoio escuro |
| Azul-acinzentado claro | #6A7E94 | Apoio médio |
| Cinza-azulado muito claro | #DCE4E9 | Bordas e divisões |
| Azul claro da foto de perfil | #D9E6F5 | Fundo de destaque claro |
| Branco | #FFFFFF | Fundo principal |
| Laranja quente | #F28C28 | Cor de destaque (botões de ação principal) |

## Regras

1. **Botão laranja: letra SEMPRE em Azul-marinho profundo #152542.** Contraste 6,2. Com letra branca o contraste cai para 2,5, e isso é proibido.
2. **Contrastes de referência para texto:** Azul-marinho profundo #152542 sobre Branco #FFFFFF = 15,3; sobre Azul claro #D9E6F5 = 12,1.
3. **Nunca indicar estado só por cor.** Sucesso, erro, aviso, ativo/inativo, selecionado: sempre use texto, ícone ou forma junto com a cor.
4. **Pequena e sóbria.** O Laranja quente #F28C28 é só para a ação principal da tela (botões). Não use laranja para decorar, para fundos, para títulos nem para ícones sem função.
5. **Não inventar cores.** Se uma tela nova precisar de uma cor fora desta paleta, não improvise: proponha a cor ao proprietário (nome, código e uso). Se for aprovada, acrescente à tabela desta skill no mesmo commit que usa a cor.

## Exceções de cor

Exceção 1: botão do WhatsApp. É a única exceção à regra do botão laranja.

- Cor: Verde WhatsApp #25D366, com letra em Azul-marinho profundo #152542. Contraste 7,7. Com letra branca o contraste cai para 2,0, e isso é proibido.
- Sempre com o ícone do WhatsApp e o texto escrito (por exemplo, "Conversar no WhatsApp"). O proprietário é daltônico, então a cor nunca é a única informação.
- Animação: pulso suave em volta do botão, para chamar atenção. A animação DEVE parar quando o aparelho estiver com "reduzir movimento" ativado (`prefers-reduced-motion: reduce`).
- Os demais botões de ação principal continuam em Laranja quente #F28C28.

Exemplo da animação:

```css
.btn-whatsapp { background:#25D366; color:#152542; animation:pulso-whatsapp 2s ease-out infinite; }
@keyframes pulso-whatsapp {
  0%   { box-shadow:0 0 0 0 rgba(37,211,102,.5); }
  70%  { box-shadow:0 0 0 12px rgba(37,211,102,0); }
  100% { box-shadow:0 0 0 0 rgba(37,211,102,0); }
}
@media (prefers-reduced-motion: reduce) { .btn-whatsapp { animation:none; } }
```

Quando surgir outra exceção de cor, proponha ao proprietário antes e registre aqui, neste mesmo commit.

## Aviso sobre o painel atual

O painel atual (`plataforma-agente.html`) ainda usa outro azul (`--accent: #1D3557`) e NÃO deve ser repintado agora. Esta skill vale para o que for criado ou alterado de agora em diante. Trocar as cores do painel é uma decisão separada, que só o proprietário toma.
