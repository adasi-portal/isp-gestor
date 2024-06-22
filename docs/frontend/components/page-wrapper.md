---
id: page-wrapper
title: Page Wrapper
---

# Page Wrapper Component

## Descrição

O componente **Page Wrapper** é uma parte fundamental do nosso projeto React, projetado para fornecer uma estrutura consistente para as páginas da aplicação. Ele é responsável por adicionar títulos, subtítulos, gerenciar o estado de carregamento (loading) e configurar metadata para SEO e compartilhamento social.

## Funcionalidades

### 1. Títulos e Subtítulos
O **Page Wrapper** permite definir títulos e subtítulos para cada página, proporcionando uma experiência de usuário coerente e melhorando a navegabilidade da aplicação.

### 2. Estado de Carregamento
O componente gerencia o estado de carregamento das páginas, exibindo indicadores visuais quando os dados estão sendo carregados, o que melhora a experiência do usuário ao informar sobre o andamento das operações.

### 3. Metadata
O **Page Wrapper** também é responsável por configurar metadata para cada página, incluindo tags de SEO e informações de compartilhamento social, garantindo que cada página tenha uma visibilidade adequada nos motores de busca e nas redes sociais.

## Estrutura do Componente

```tsx
import React from 'react';
import PropTypes from 'prop-types';
import { Helmet } from 'react-helmet';
import LoadingComponent from './LoadingComponent';

interface IProps {
  title: string;
  subtitle?: string;
  isLoading?: boolean;
  children: React.ReactNode;
}

const PageWrapper: React.FC<IProps> = ({
  title,
  subtitle,
  isLoading = false,
  children
}) => {
  return (
    <div className="page-wrapper">
      <Helmet>
        <title>{title}</title>
        <meta name="description" content={subtitle} />
        <meta property="og:title" content={title} />
        <meta property="og:description" content={subtitle} />
      </Helmet>
      {isLoading ? (
        <LoadingComponent />
      ) : (
        <div>
          <h1>{title}</h1>
          <h2>{subtitle}</h2>
          {children}
        </div>
      )}
    </div>
  );
};


export default PageWrapper;
```

### Propriedades

- title (`string`, obrigatório): O título da página. Será exibido na tag `<title>` do HTML e nos títulos da página.
- subtitle (`string`, opcional): O subtítulo da página. Será usado para metadata e exibido como subtítulo.
- isLoading (`bool`, opcional): Indica se a página está em estado de carregamento. Quando true, um spinner de carregamento é exibido.
- children (`node`, obrigatório): O conteúdo da página que será renderizado dentro do wrapper.

### Uso

Exemplo de uso do Page Wrapper em uma página:

```typescript
import React, { useState, useEffect } from 'react';
import PageWrapper from './components/PageWrapper';

const HomePage = () => {
  const [isLoading, setIsLoading] = useState(true);

  useEffect(() => {
    // Simula carregamento de dados
    setTimeout(() => {
      setIsLoading(false);
    }, 2000);
  }, []);

  return (
    <PageWrapper title="Home Page" subtitle="Welcome to our website" isLoading={isLoading}>
      <p>This is the content of the home page.</p>
    </PageWrapper>
  );
};

export default HomePage;
```

### Contribuição

Contribuições para melhorias no componente **Page Wrapper** são bem-vindas. Por favor, siga as diretrizes de contribuição do projeto e abra um pull request com suas mudanças.
