# 🛍️ Catálogo Digital de Vendas com Pedidos via WhatsApp

Um projeto moderno, elegante e responsivo de **catálogo de produtos e pedidos diretos para o WhatsApp**, pronto para ser publicado no **GitHub Pages** de forma 100% gratuita, sem necessidade de servidores, bancos de dados ou processos complexos de build.

---

## ✨ Funcionalidades Principais

- ⚡ **Zero Configuração de Servidor:** Funciona diretamente no GitHub Pages como uma SPA (Single Page Application) em HTML5, Tailwind CSS e Vanilla JavaScript.
- 💬 **Checkout Direto no WhatsApp:** O cliente monta o pedido, adiciona itens ao carrinho, preenche os dados de entrega/retirada, forma de pagamento e clica em **"Enviar Pedido no WhatsApp"**. Uma mensagem perfeitamente formatada é enviada direto para o WhatsApp comercial da sua loja!
- 🔍 **Busca em Tempo Real & Filtros:** Busca instantânea por nome, descrição ou categoria, filtro por promoções e ordenação por preço, avaliação ou nome.
- 📱 **100% Responsivo & Mobile-First:** Perfeito tanto em smartphones (onde a maioria das compras acontece) quanto em tablets e computadores.
- 🎨 **Modo Escuro / Claro:** Alternância suave entre tema dark e light com memorização da preferência do cliente.
- ❤️ **Lista de Favoritos (Wishlist):** Permite aos clientes marcarem itens favoritos para comprar depois (salvos no `localStorage`).
- 🏷️ **Cupons de Desconto:** Suporte a cupons promocionais (ex: `AURORA10` para 10% OFF, `VIP15` para 15% OFF).
- ⚙️ **Painel de Configuração Rápida:** Botão de engrenagem integrado na página para testar troca de WhatsApp, nome da loja e chave Pix em tempo real.
- 🖨️ **Impressão / Cópia de Comprovante:** Gera resumo copiável para a área de transferência e comprovante formatado para impressão ou PDF.

---

## 🚀 Como Publicar no GitHub Pages (Passo a Passo)

Publicar seu catálogo no GitHub leva menos de 3 minutos:

### Passo 1: Criar o Repositório no GitHub
1. Acesse [github.com](https://github.com/) e faça login na sua conta.
2. Clique no botão **"New"** (Novo repositório) no canto superior direito.
3. Escolha um nome para o repositório (exemplo: `catalogo-vendas` ou `loja-virtual`).
4. Deixe o repositório como **Public** (Público).
5. Clique em **"Create repository"**.

### Passo 2: Fazer Upload dos Arquivos
1. Na página do repositório recém-criado, clique no link **"uploading an existing file"**.
2. Arraste e solte o arquivo `index.html` e o `README.md` para a página.
3. No final da tela, clique no botão verde **"Commit changes"**.

### Passo 3: Ativar o GitHub Pages
1. No seu repositório, clique na aba **"Settings"** (Configurações).
2. No menu lateral esquerdo, clique em **"Pages"**.
3. Na seção **"Build and deployment"** > **"Branch"**:
   - Selecione a branch `main` (ou `master`).
   - Mantenha a pasta como `/ (root)`.
   - Clique em **"Save"**.
4. Aguarde cerca de 1 a 2 minutos. O GitHub exibirá uma caixa verde com o link da sua página:
   ```text
   Your site is live at https://seu-usuario.github.io/catalogo-vendas/
   ```

---

## ⚙️ Como Personalizar para o seu Negócio

Abra o arquivo `index.html` em qualquer editor de código (como VS Code, Notepad++ ou diretamente no editor web do GitHub):

### 1. Alterar o Número do WhatsApp e Dados da Loja
No início da tag `<script>` (por volta da linha 450 do `index.html`), você encontrará a constante `DEFAULT_CONFIG`:

```javascript
const DEFAULT_CONFIG = {
  storeName: 'Minha Loja',                // Nome da sua loja
  whatsapp: '5511999999999',              // DDI (55) + DDD (11) + Celular (somente números)
  pixKey: 'pix@minhaloja.com.br',         // Sua chave Pix para pagamento
  announcement: '🚀 Frete Grátis acima de R$ 199 | Parcelamento em até 10x sem juros'
};
```

> **Atenção:** Coloque o número do WhatsApp com o código do país (55 para o Brasil) e DDD, sem espaços, hífens ou parênteses. Exemplo: `5511987654321`.

### 2. Cadastrar / Modificar Produtos
Logo abaixo da configuração, você encontrará a lista de produtos na constante `PRODUCTS`:

```javascript
{
  id: 'meu-produto-1',
  name: 'Nome do Seu Produto',
  category: 'tecnologia',              // categoria: tecnologia, moda, casa, acessorios
  categoryName: 'Tecnologia',          // nome visível da categoria
  price: 199.90,                       // preço de venda
  originalPrice: 249.90,               // preço original (se tiver promoção)
  installments: '10x de R$ 19,99 sem juros',
  rating: 5.0,                         // avaliação (1.0 a 5.0)
  reviewsCount: 35,                    // número de avaliações
  badge: 'Destaque',                   // tag em destaque (ex: Novo, Oferta, Mais Vendido)
  badgeColor: 'bg-brand-600',          // cor da tag
  image: 'https://seusite.com/imagem.jpg', // URL da imagem ou caminho relativo
  description: 'Descrição completa do produto destacando benefícios.',
  specs: [
    'Característica técnica 1',
    'Característica técnica 2',
    'Garantia de 1 ano'
  ],
  options: ['Preto', 'Branco']         // variações (tamanhos, cores, voltagens)
}
```

### 3. Usar suas Próprias Imagens
Você tem duas formas simples de adicionar suas fotos:
- **Opção A (Imagens no próprio GitHub):** Crie uma pasta chamada `img` no seu repositório, coloque as fotos dos seus produtos lá (ex: `img/produto1.jpg`) e no array coloque `image: 'img/produto1.jpg'`.
- **Opção B (Links externos):** Use links de imagens hospedadas em serviços como Imgur, Cloudinary ou em seu próprio site.

---

## 💡 Dicas para Aumentar suas Vendas no WhatsApp

1. **Coloque o link do GitHub Pages na Bio do Instagram:** Utilize o link do catálogo na bio do seu perfil e stories para direcionar os seguidores direto para a vitrine.
2. **Responda rápido:** O catálogo já entrega o pedido com o nome do cliente, endereço, itens e valor total somado. Quando receber a mensagem, envie a confirmação e a chave Pix de imediato.
3. **Ofereça cupons de primeira compra:** Divulgue o cupom `AURORA10` ou crie cupons personalizados na função de cupons do código.

---

## 📄 Licença
Este projeto é de código aberto e livre para uso pessoal e comercial. Sinta-se à vontade para modificar e adaptar à sua marca!
