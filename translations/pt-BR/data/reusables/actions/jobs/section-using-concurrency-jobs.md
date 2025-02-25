---
ms.openlocfilehash: e0ae7814db2deb2c1e666172e71566cc6d28ca1b
ms.sourcegitcommit: 47bd0e48c7dba1dde49baff60bc1eddc91ab10c5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/05/2022
ms.locfileid: "145085279"
---
{% note %}

**Observação:** quando a simultaneidade é especificada no nível do trabalho, a ordem não é garantida para execuções ou trabalhos que são colocados na fila em intervalos de cinco minutos com relação um ao outro.

{% endnote %}

Você pode usar `jobs.<job_id>.concurrency` para garantir que apenas um trabalho ou fluxo de trabalho que usa o mesmo grupo de simultaneidade seja executado por vez. Um grupo de concorrência pode ser qualquer string ou expressão. A expressão pode usar qualquer contexto, exceto o contexto `secrets`. Para obter mais informações sobre expressões, confira "[Expressões](/actions/learn-github-actions/expressions)".

Especifique também `concurrency` no nível do fluxo de trabalho. Para obter mais informações, confira [`concurrency`](/actions/using-workflows/workflow-syntax-for-github-actions#concurrency).

{% data reusables.actions.actions-group-concurrency %}
