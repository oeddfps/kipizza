# 🍕 KI Pizza - Guia de Deployment no Render

## ✅ Problema Resolvido

O erro "Not Found" acontecia porque:
1. **Arquivo principal**: chamava-se `index-2.html` em vez de `index.html`
2. **Configuração**: Publish Directory precisava apontar para `xhtml`

## 📋 Configuração do Render Static Site

Use estas configurações EXATAS no Render:

```
Name: kipizza
Branch: main (ou master, dependendo do seu Git)
Root Directory: (deixar VAZIO)
Build Command: (deixar VAZIO)
Publish Directory: xhtml
```

## 🔍 Arquivos de Debug Criados

1. **xhtml/index.html** - Arquivo principal (cópia do index-2.html) com logs de debug
2. **xhtml/404.html** - Página customizada de erro com diagnóstico
3. **render.yaml** - Configuração automática do Render

## 📊 Logs no Console do Navegador

Após o deploy, abra o Console do navegador (F12) e você verá:
- ✅ Logs de inicialização
- ✅ URL e informações de navegação
- ✅ Erros de carregamento de recursos (se houver)
- ✅ Status do DOM e carregamento completo

## 🚀 Como fazer Deploy

### Opção 1: Via Git (Recomendado)

```bash
# Se ainda não inicializou o Git
cd "c:\Users\Edson NF\Downloads\sitep\Restroking-v1.1.1-24_February_2025"
git init
git add .
git commit -m "Deploy Ki Pizza - versão com logs"

# Conectar com repositório remoto (GitHub/GitLab)
git remote add origin SEU_REPOSITORIO_URL
git push -u origin main
```

### Opção 2: Via Dashboard do Render

1. Acesse: https://dashboard.render.com/
2. Clique em "New +" > "Static Site"
3. Conecte seu repositório Git
4. Use as configurações acima
5. Clique em "Create Static Site"

## 🐛 Troubleshooting

### Se ainda aparecer "Not Found":

1. **Verifique o console do navegador** (F12) - os logs vão mostrar o que está acontecendo
2. **Limpe o cache**: Ctrl + Shift + R (Windows) ou Cmd + Shift + R (Mac)
3. **Verifique os logs do Render**: No dashboard do Render > Seu projeto > Logs
4. **Teste a página 404**: Acesse `seu-site.onrender.com/pagina-que-nao-existe` para ver o debug

### Checklist de Verificação:

- [ ] Arquivo `xhtml/index.html` existe?
- [ ] Publish Directory está como `xhtml`?
- [ ] Root Directory está VAZIO?
- [ ] Branch está correto (main ou master)?
- [ ] Git push foi feito com sucesso?
- [ ] Deploy finalizou sem erros no Render?

## 📞 Informações do Site

- **Region**: Teutônia, RS
- **WhatsApp**: 51 9707-6997
- **Instagram**: https://www.instagram.com/kipizzateutonia/
- **Delivery**: https://pedido.anota.ai/ki.pizza
- **Endereço**: R. Evaldo Schaefer, 1448 - Canabarro, Teutônia - RS, 95890-000

## 📝 Placeholders ainda para substituir:

Procure e substitua no arquivo `xhtml/index.html`:
- `{TELEFONE}` - Telefone fixo (se houver)
- `{EMAIL}` - Email de contato
- `{NOME_MARCA}` - "Ki Pizza" ou nome completo
- `{QTD_SABORES}` - Quantidade de sabores no rodízio
- `{DURACAO_RODIZIO}` - Duração do rodízio (ex: "2h", "livre")
- `{URL_CARDAPIO}` - Link para PDF do cardápio (se houver)

## ✅ Status Atual

- [x] index.html criado (cópia do index-2.html)
- [x] Logs de debug adicionados
- [x] Arquivo 404.html criado
- [x] render.yaml configurado
- [x] README de deployment criado
- [ ] Deploy no Render
- [ ] Testar no navegador
- [ ] Substituir placeholders restantes
