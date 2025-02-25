---
title: Gerenciando sua função em uma organização pertencente à sua empresa
intro: Você pode gerenciar a sua ssoviação em qualquer organização pertencente à sua empresa e mudar sua função dentro da organização.
permissions: Enterprise owners can manage their role in an organization owned by the enterprise.
versions:
  feature: enterprise-owner-join-org
type: how_to
topics:
  - Administrator
  - Enterprise
  - Organizations
shortTitle: Manage your organization roles
ms.openlocfilehash: e7a95602fe103dcbccb80bc2dfec6a67f8b4b312
ms.sourcegitcommit: 47bd0e48c7dba1dde49baff60bc1eddc91ab10c5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/05/2022
ms.locfileid: '147065175'
---
## Sobre o gerenciamento de funções

Você pode optar por participar de uma organização pertencente à sua empresa como integrante ou como proprietário da organização, mudar a sua função dentro da organização ou sair da organização.

{% ifversion ghec %} {% warning %}

**Aviso**: se uma organização usa o SCIM para provisionar usuários, o ingresso na organização dessa forma pode ter consequências não intencionais. Para obter mais informações, confira "[Sobre o SCIM para organizações](/organizations/managing-saml-single-sign-on-for-your-organization/about-scim-for-organizations)".

{% endwarning %} {% endif %}

Para obter informações sobre como gerenciar as funções de outras pessoas em uma organização, confira "[Como gerenciar a associação em sua organização](/organizations/managing-membership-in-your-organization)" e "[Como gerenciar o acesso das pessoas com funções à sua organização](/organizations/managing-peoples-access-to-your-organization-with-roles)".

## Gerenciando seu papel com as configurações corporativas

Você pode participar de uma organização pertencente à sua empresa e gerenciar sua função na organização, diretamente nas configurações da conta corporativa.

{% ifversion ghec %}

Se uma organização aplivar o logon único do SAML (SSO), você não poderá usar as configurações corporativas para participar da organização. Em vez disso, você deve participar da organização usando o provedor de identidade (IdP) dessa organização. Em seguida, você pode gerenciar a sua função nas configurações da sua empresa. Para obter mais informações, confira "[Como ingressar em uma organização que impõe o SSO do SAML](#joining-an-organization-that-enforces-saml-sso)".

{% endif %}

{% data reusables.enterprise-accounts.access-enterprise %}
1. Na guia **Organizações**, à direita da organização na qual deseja gerenciar sua função, selecione o menu suspenso {% octicon "gear" aria-label="The gear icon" %} e clique na ação que deseja executar.

   ![Captura de tela do menu suspenso para o ícone de engrenagem de uma organização](/assets/images/help/business-accounts/change-role-in-org.png)

{% ifversion ghec %}

## Entrando para uma organização que apliva o SAML SSO

Se uma organização aplicar o SSO SAML, você não poderá usar as configurações da empresa para participar da organização. Em vez disso, você deve participar da organização usando o provedor de identidade (IdP) dessa organização.

1. Você deve ter acesso no seu IdP para o aplicativo {% data variables.product.prodname_ghe_cloud %} que é usado pela organização. Se você não conseguir configurar seu IdP, entre em contato com o administrador do seu IdP.
1. Efetuar a autentivação na organização usando o SAML SSO.

   - Se a organização usar o SCIM, aceite o convite da organização que será gerado pela integração do SCIM.
   - Se a organização não usar o SCIM, acesse o URL a seguir, substituindo a ORGANIZAÇÃO pelo nome da organização e, em seguida, siga as instruções para efetuar a autenticação.

    `https://github.com/orgs/ORGANIZATION/sso`

Depois de entrar na organização, você poderá usar as configurações corporativas para gerenciar a sua função na organização como, por exemplo, se tornar proprietário da organização. Para obter mais informações, confira "[Como gerenciar sua função com as configurações da empresa](#managing-your-role-with-the-enterprise-settings)".

{% endif %}
