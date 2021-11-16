---
title: Activar o desactivar Microsoft Forms
ms.author: jokay
author: dumptruckjon
manager: kathyl
audience: Admin
ms.topic: how-to
ms.service: forms-pro
ms.localizationpriority: high
description: En este artículo se explica cómo los administradores de Microsoft 365 pueden desactivar o activar Microsoft Forms para toda la organización o personas específicas de su organización.
ms.openlocfilehash: 2d1280bd7d61dc8b31cfb84dfeaced2662603e4f
ms.sourcegitcommit: 09bdc82ce67e74495b6c58d9c842e31c17956fc3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2021
ms.locfileid: "60951530"
---
# <a name="turn-off-or-turn-on-microsoft-forms"></a>Activar o desactivar Microsoft Forms

De forma predeterminada, [Microsoft Forms](https://support.microsoft.com/office/what-is-microsoft-forms-6b391205-523c-45d2-b53a-fc10b22017c8) está activado para todos los usuarios de la organización. Si es un [administrador](https://support.microsoft.com/topic/eac4d046-1afd-4f1a-85fc-8219c79e1504), puede [configurar Microsoft Forms](https://support.microsoft.com/office/set-up-microsoft-forms-cc52287a-4550-464d-9a1b-457bf9df2240) y desactivarlo o volver a activarlo para toda la organización o solo para personas específicas.

## <a name="turn-off-microsoft-forms-for-everyone-in-your-organization"></a>Desactivar Microsoft Forms para todos los miembros de la organización

1.  Inicie sesión en [Microsoft Azure](https://portal.azure.com/).

2.  Seleccione **Azure Active Directory** en el panel izquierdo.

3.  Haga clic en **Aplicaciones empresariales.**

4.  Vaya a los servicios necesarios y repita los pasos 5 a 7 para **Tipo de aplicación**\> **CollabDBService** y **Aplicaciones de Microsoft** \> **Microsoft Forms**.
    
      - En el campo de búsqueda de la lista desplegable **Tipo de aplicación**, escriba **CollabDBService**. Seleccione **CollabDBService** en la lista de resultados de búsqueda.
    
      - En la lista desplegable **Tipo de aplicación**, seleccione **Aplicaciones de Microsoft**. En el campo de búsqueda de la lista desplegable **Tipo de aplicación**, escriba **Microsoft Forms** y seleccione **Microsoft Forms** en la lista de resultados de búsqueda.

5.  En **Administrar**, haga clic en **Propiedades**.

6.  Para la opción **¿Habilitado para que los usuarios inicien sesión?**, seleccione **No**.

7.  Haga clic en **Guardar**.

## <a name="turn-off-microsoft-forms-for-specific-people-in-your-organization"></a>Desactivar Microsoft Forms para personas específicas de su organización

1.  Inicie sesión en Microsoft 365 con su cuenta profesional o educativa como administrador global. [Descubra cómo iniciar sesión](https://support.microsoft.com/office/where-to-sign-into-microsoft-365-for-business-e9eb7d51-5430-4929-91ab-6157c5a050b4).

2.  En el Centro de administración de Microsoft 365, haga clic en **Usuarios ** \> **Usuarios activos**.

3.  Seleccione la casilla situada junto al nombre de la persona para la que quiere desactivar Microsoft Forms.

4.  En la cinta de opciones, haga clic en **Administrar licencias de producto**.

5.  En el formulario de cuenta que se abre, en la pestaña **Licencias y aplicaciones**, expanda la sección Aplicaciones y desplácese hacia abajo hasta la opción Microsoft Forms. 

    :::image type="content" source="./media/turn-forms-off-on-licenses-apps.jpg" alt-text="Formulario Opciones de cuenta en el Centro de administración de Microsoft 365":::

6.  Desmarque la casilla para desactivar Microsoft Forms. Para activarlo, marque la casilla.

    :::image type="content" source="./media/turn-forms-off-on-plan-e1.jpg" alt-text="Botón de alternancia de Microsoft Forms":::

     > [!Note]
     > [Consulte esta lista](https://support.microsoft.com/office/office-licenses-that-include-microsoft-forms-efa14679-5d99-47c5-bdf1-2fc838767f7e) para ver si tiene una licencia de Office que incluya Microsoft Forms. Si aparece la licencia, deberá desactivar la casilla de Microsoft Forms para desactivar completamente el acceso de usuario.

7.  En la parte inferior de la lista de **Aplicaciones**, haga clic en **Guardar cambios**.

## <a name="i-turned-on-microsoft-forms-but-people-in-my-organization-still-cant-access-it"></a>He activado Microsoft Forms, pero los usuarios de mi organización siguen sin poder acceder

Compruebe la siguiente configuración en Microsoft Azure para asegurarse de que Microsoft Forms está habilitado:

1.  Inicie sesión en [Microsoft Azure](https://portal.azure.com/).

2.  Seleccione **Azure Active Directory** en el panel izquierdo.

3.  Haga clic en **Aplicaciones empresariales.**

4.  Vaya a los servicios necesarios y repita los pasos 5 a 7 para **Tipo de aplicación**\> **CollabDBService** y **Aplicaciones de Microsoft** \> **Microsoft Forms**.
    
      - En el campo de búsqueda de la lista desplegable **Tipo de aplicación**, escriba **CollabDBService**. Seleccione **CollabDBService** en la lista de resultados de búsqueda.
    
      - En la lista desplegable **Tipo de aplicación**, seleccione **Aplicaciones de Microsoft**. En el campo de búsqueda de la lista desplegable **Tipo de aplicación**, escriba **Microsoft Forms** y seleccione **Microsoft Forms** en la lista de resultados de búsqueda.

5.  En **Administrar**, haga clic en **Propiedades**.

6.  Para la opción **¿Habilitado para que los usuarios inicien sesión?**, seleccione **Sí**.

7.  Haga clic en **Guardar**.

    >[!Note]
    >Los servicios de SharePoint también deben estar habilitados para que los usuarios de su organización puedan acceder a Microsoft Forms.

## <a name="feedback-for-microsoft-forms"></a>Comentarios sobre Microsoft Forms

Queremos escuchar sus comentarios\! Para enviar comentarios sobre MicrosoftForms, vaya a la esquina superior derecha del formulario y seleccione **Más opciones del formulario** ![Botón Más opciones](./media/image2.png)\> **Comentarios**.

