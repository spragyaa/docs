---
ms.openlocfilehash: 005667bae249af732a73e5afc53e7dcd7ae436fe
ms.sourcegitcommit: 47bd0e48c7dba1dde49baff60bc1eddc91ab10c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/05/2022
ms.locfileid: "145084668"
---
{% ifversion ghes %}
### 支持 2FA 的身份验证方法

| 身份验证方法 | 说明  | 双重身份验证支持 |
|-----------------------|--------------|-----------------------------------|
| 内置 | 根据存储在 {% data variables.product.prodname_ghe_server %} 设备上的个人帐户进行身份验证。 | 在 {% data variables.product.prodname_ghe_server %} 设备上支持和管理。 组织管理员可要求对组织的成员启用 2FA。 |{% ifversion ghes %}
| 内置向身份提供商进行身份验证| 根据存储在标识提供者中的帐户进行身份验证。 | 依赖身份提供程序。{% endif %}
| LDAP | 允许与您的公司目录服务集成以进行身份验证。 | 在 {% data variables.product.prodname_ghe_server %} 设备上支持和管理。 组织管理员可要求对组织的成员启用 2FA。 |
| SAML | 在外部身份提供商上进行身份验证。 | {% data reusables.two_fa.2fa_not_supported_with_saml_and_cas %} |
| CAS | 单点登录服务由外部服务器提供。 | {% data reusables.two_fa.2fa_not_supported_with_saml_and_cas %}{% endif %}
