# Sugestões Técnicas para WordPress: Landing Page de Ativos Virtuais

## 1. Plugins Recomendados para Infográficos e Elementos Visuais

### 1.1 Elementor Pro
O Elementor Pro é uma das melhores opções para criar infográficos e elementos visuais diretamente no WordPress. Oferece:
- **Widget de Imagem Interativa**: Permite adicionar hotspots clicáveis nos infográficos
- **Widget de Contador**: Ideal para estatísticas sobre ativos virtuais
- **Widget de Linha do Tempo**: Perfeito para mostrar a evolução da regulamentação
- **Widget de Tabela**: Para comparações entre DLTs permissionadas e não permissionadas

### 1.2 Infogram
Plugin que permite integrar infográficos criados na plataforma Infogram:
- Gráficos interativos sobre capitalização de mercado
- Mapas para mostrar adoção global de ativos virtuais
- Diagramas de fluxo para explicar mecanismos de consenso

### 1.3 WP Charts and Graphs
Para criar gráficos e visualizações de dados:
- Gráficos de pizza para distribuição de tipos de DLT
- Gráficos de barras para comparar escalabilidade
- Gráficos de linha para mostrar evolução temporal

### 1.4 Ultimate Blocks
Oferece blocos específicos para conteúdo educativo:
- Bloco de Tabela de Conteúdo
- Bloco de Accordion para FAQ
- Bloco de Call-to-Action para destacar informações importantes

## 2. Estrutura de Menu Recomendada

### 2.1 Menu Principal
```
Home
├── Ativos Virtuais
│   ├── Definição Legal
│   ├── Tipos de Ativos
│   └── Regulamentação
├── Reserva de Valor
│   ├── Bitcoin e Escassez
│   ├── Stablecoins
│   └── Mecanismos de Lastro
├── Tecnologias
│   ├── DLT Permissionadas
│   ├── DLT Não Permissionadas
│   ├── Escalabilidade
│   ├── Segurança
│   └── Governança
├── Contratos Inteligentes
│   ├── Conceitos Básicos
│   ├── Eficiência
│   ├── Inclusão Financeira
│   └── Casos de Uso
└── Recursos
    ├── Bibliografia
    ├── Glossário
    └── Links Úteis
```

### 2.2 Menu Secundário (Footer)
```
Sobre o Projeto
Metodologia
Fontes Acadêmicas
Contato
Política de Privacidade
```

## 3. Blocos Visuais Recomendados

### 3.1 Bloco de Definição Legal
**Plugin**: Custom Post Type UI + Advanced Custom Fields
- Campo para texto da lei
- Campo para data de publicação
- Campo para link oficial
- Campo para resumo executivo

### 3.2 Bloco de Comparação DLT
**Plugin**: TablePress
- Tabela comparativa entre DLTs permissionadas e não permissionadas
- Colunas: Característica, Permissionada, Não Permissionada, Impacto no SFN
- Filtros por categoria (Escalabilidade, Segurança, Governança)

### 3.3 Bloco de Infográfico Interativo
**Plugin**: H5P
- Imagens interativas com hotspots
- Quiz sobre conceitos de ativos virtuais
- Linha do tempo interativa da regulamentação

### 3.4 Bloco de Citação Acadêmica
**Plugin**: Custom CSS + Gutenberg
```css
.academic-quote {
    border-left: 4px solid #667eea;
    background: #f8f9fa;
    padding: 1.5rem;
    margin: 2rem 0;
    font-style: italic;
    position: relative;
}

.academic-quote::before {
    content: '"';
    font-size: 4rem;
    color: #667eea;
    position: absolute;
    top: -10px;
    left: 10px;
}

.academic-quote .source {
    font-weight: bold;
    margin-top: 1rem;
    font-style: normal;
}
```

## 4. Configurações de SEO e Performance

### 4.1 Plugin Yoast SEO
Configurações específicas para conteúdo educativo:
- **Palavra-chave principal**: "ativos virtuais lei 14.478"
- **Meta descrição**: "Guia acadêmico completo sobre ativos virtuais, DLTs e contratos inteligentes baseado na Lei 14.478/2022"
- **Schema markup**: Article + EducationalOrganization

### 4.2 Plugin WP Rocket
Otimizações para infográficos:
- Lazy loading para imagens grandes
- Compressão de imagens
- Minificação de CSS/JS
- Cache de página

### 4.3 Plugin Smush
Para otimização de infográficos:
- Compressão automática de PNG
- Conversão para WebP
- Redimensionamento responsivo

## 5. Customizações de CSS

### 5.1 Estilo para Seções Acadêmicas
```css
.academic-section {
    background: white;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    padding: 3rem;
    margin: 2rem 0;
    transition: transform 0.3s ease;
}

.academic-section:hover {
    transform: translateY(-5px);
}

.academic-section h2 {
    color: #667eea;
    border-bottom: 3px solid #667eea;
    padding-bottom: 0.5rem;
    margin-bottom: 1.5rem;
}
```

### 5.2 Estilo para Infográficos
```css
.infographic-container {
    text-align: center;
    margin: 2rem 0;
    padding: 2rem;
    background: #f8f9fa;
    border-radius: 10px;
}

.infographic-container img {
    max-width: 100%;
    height: auto;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    transition: transform 0.3s ease;
}

.infographic-container img:hover {
    transform: scale(1.05);
}
```

### 5.3 Estilo para Navegação Sticky
```css
.sticky-nav {
    position: sticky;
    top: 0;
    z-index: 1000;
    background: rgba(255,255,255,0.95);
    backdrop-filter: blur(10px);
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}
```

## 6. Funcionalidades JavaScript

### 6.1 Smooth Scrolling
```javascript
// Adicionar ao functions.php do tema
function add_smooth_scrolling() {
    ?>
    <script>
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            document.querySelector(this.getAttribute('href')).scrollIntoView({
                behavior: 'smooth'
            });
        });
    });
    </script>
    <?php
}
add_action('wp_footer', 'add_smooth_scrolling');
```

### 6.2 Animações de Entrada
```javascript
// Intersection Observer para animações
const observerOptions = {
    threshold: 0.1,
    rootMargin: '0px 0px -50px 0px'
};

const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            entry.target.classList.add('animate-in');
        }
    });
}, observerOptions);

document.querySelectorAll('.academic-section').forEach(el => {
    observer.observe(el);
});
```

## 7. Configuração de Tema Child

### 7.1 Estrutura de Arquivos
```
tema-ativos-virtuais/
├── style.css
├── functions.php
├── header.php
├── footer.php
├── single-ativo-virtual.php
├── page-glossario.php
├── assets/
│   ├── css/
│   │   └── academic.css
│   ├── js/
│   │   └── interactions.js
│   └── images/
│       └── infograficos/
└── templates/
    ├── section-definicao.php
    ├── section-reserva-valor.php
    ├── section-dlt.php
    └── section-contratos.php
```

### 7.2 Functions.php Customizado
```php
<?php
// Enqueue styles and scripts
function academic_theme_assets() {
    wp_enqueue_style('academic-style', get_stylesheet_directory_uri() . '/assets/css/academic.css');
    wp_enqueue_script('academic-interactions', get_stylesheet_directory_uri() . '/assets/js/interactions.js', array('jquery'), '1.0', true);
}
add_action('wp_enqueue_scripts', 'academic_theme_assets');

// Custom post type for academic content
function create_academic_post_types() {
    register_post_type('ativo_virtual',
        array(
            'labels' => array(
                'name' => 'Ativos Virtuais',
                'singular_name' => 'Ativo Virtual'
            ),
            'public' => true,
            'supports' => array('title', 'editor', 'thumbnail', 'custom-fields'),
            'menu_icon' => 'dashicons-chart-line'
        )
    );
}
add_action('init', 'create_academic_post_types');
```

## 8. Plugins de Acessibilidade

### 8.1 WP Accessibility
Para garantir conformidade com WCAG:
- Alt text automático para infográficos
- Navegação por teclado
- Contraste de cores adequado
- Leitores de tela compatíveis

### 8.2 UserWay Accessibility Widget
Widget de acessibilidade que oferece:
- Ajuste de tamanho de fonte
- Alto contraste
- Navegação por voz
- Tradução automática

## 9. Integração com Ferramentas Acadêmicas

### 9.1 Plugin Zotero
Para gerenciamento de referências:
- Importação automática de citações
- Formatação ABNT
- Bibliografia dinâmica

### 9.2 Plugin Academic Blogger's Toolkit
Para funcionalidades acadêmicas:
- Notas de rodapé automáticas
- Citações inline
- Índice de autores
- Glossário automático

## 10. Monitoramento e Analytics

### 10.1 Google Analytics 4
Configuração específica para conteúdo educativo:
- Eventos de engajamento com infográficos
- Tempo de leitura por seção
- Downloads de materiais
- Compartilhamentos sociais

### 10.2 Hotjar
Para análise de comportamento:
- Heatmaps de infográficos
- Gravações de sessão
- Feedback de usuários
- Testes A/B de layout

Esta estrutura técnica garante que a landing page sobre ativos virtuais seja não apenas informativa e academicamente rigorosa, mas também tecnicamente robusta e acessível a todos os usuários.

