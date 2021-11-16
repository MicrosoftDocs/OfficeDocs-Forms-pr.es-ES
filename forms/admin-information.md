---
title: Información de administración
ms.author: jokay
author: dumptruckjon
manager: kathyl
audience: Admin
ms.topic: how-to
ms.service: forms-pro
ms.localizationpriority: high
description: En este artículo, se responden las preguntas más frecuentes sobre la información de administración de Microsoft Forms.
ms.openlocfilehash: 3fed9f104b6a44a7c23221b204796b22c8fb5109
ms.sourcegitcommit: 09bdc82ce67e74495b6c58d9c842e31c17956fc3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2021
ms.locfileid: "60951563"
---
# <a name="admin-information"></a>Información de administración

## <a name="getting-started"></a>Introducción

**¿Cómo desactivar o activar Microsoft Forms?**

De forma predeterminada, Microsoft Forms está activado para todos los usuarios de una organización. Los administradores de TI de Microsoft365 pueden desactivar Microsoft Forms en el Centro de administración de Microsoft365, en la pestaña **Administración de usuarios**. Consulte [Configurar Microsoft Forms](set-up-microsoft-forms.md) y [Desactivar o activar Microsoft Forms](turn-off-turn-on-microsoft-forms.md) para más información.

**¿Cómo permitir el acceso a Microsoft Forms solo a personas específicas de mi organización?**

Los administradores pueden cambiar los permisos de acceso para personas específicas de la organización. Vea [Configuración de administrador en Microsoft Forms](administrator-settings-microsoft-forms.md).

## <a name="data-storage"></a>Almacenamiento de datos

**¿Dónde se almacenan los datos de Microsoft Forms?**

Los datos de Microsoft Forms se almacenan en servidores de Estados Unidos, a excepción de los datos para espacios empresariales de Europa. Los datos de espacios empresariales de Europa se almacenan en servidores de Europa.

## <a name="user-activity"></a>Actividad de usuario

**¿Cómo ver las actividades realizadas en Microsoft Forms por personas de mi organización?**

Puede revisar las [actividades de Microsoft Forms](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance?view=o365-worldwide#microsoft-forms-activities) en el registro de auditoría del [Centro de seguridad de Microsoft 365](https://security.microsoft.com/?rfr=OfficeScc). Obtenga más información sobre la [Auditoría en Office 365 (para administradores)](https://support.microsoft.com/topic/auditing-in-office-365-for-admins-9f6484d2-0fd2-17de-165f-c41346023906).

## <a name="user-account-information"></a>Información de la cuenta de usuario

**¿Cómo comprobar si una cuenta de usuario se ha "eliminado permanentemente"?**

1. Los administradores pueden iniciar sesión en [Microsoft Graph](https://developer.microsoft.com/graph/graph-explorer).

2. En el cuadro de búsqueda superior, pegue la siguiente dirección URL:

   `https://graph.microsoft.com/v1.0/directory/deletedItems/microsoft.graph.user?$filter=mail eq '*user email*'`

   >[!Note]
   >*correo electrónico de usuario* = dirección de correo electrónico del propietario del formulario que ha dejado la organización o cuya cuenta se ha deshabilitado.

3. Haga clic en **Ejecutar consulta**.

Si la información de la cuenta que busca se devuelve en la consulta, significa que la cuenta se ha eliminado temporalmente y está dentro del límite de 30 días. Un administrador global puede transferir los formularios que pertenecen a la cuenta eliminada temporalmente mediante el método de transferencia descrito anteriormente.

Si la información de la cuenta que busca no se devuelve en la consulta, significa que la cuenta sigue existiendo en el espacio empresarial de Office 365 o se eliminó hace más de 30 días. Si la cuenta existe o está deshabilitada en el inquilino de Office 365, un administrador global puede transferir los formularios que pertenecen a la cuenta. Si la cuenta se ha "eliminado permanentemente" desde el espacio empresarial de Office 365, un administrador global no podrá transferir los formularios que eran propiedad de esa cuenta. Estos formularios tampoco se pueden recuperar.

**¿Existe un límite en el número de usuarios y en la cantidad de datos que se almacenan para las cuentas de usuario incluso después de que hayan dejado la organización?**

De momento, no existe un límite de usuarios para los que se conservan los datos, siempre que el aprovisionamiento de sus cuentas esté dentro del contrato de servicio en línea de la organización. Tampoco existe un límite de cantidad de datos almacenados para cuentas de usuario.

**¿Qué ocurre con los datos de un formulario si se ha quitado la licencia de Microsoft Forms del propietario o si el usuario está deshabilitado o se ha eliminado de su inquilino (Azure AD)?**

Si se ha quitado la licencia del propietario o la cuenta del propietario está deshabilitada, no hay ningún cambio en la cantidad de datos almacenados para la cuenta de usuario.

Si se ha eliminado una cuenta de usuario del inquilino (Azure AD), todos los datos relacionados con la cuenta se eliminarán 30 días después de que se haya eliminado el usuario.

## <a name="form-ownership-transfer"></a>Transferencia de propiedad del formulario

**El propietario original de un formulario ya no está en mi organización. ¿Cómo puedo transferir la propiedad de su formulario?**

Para transferir el formulario de alguien que ha dejado la organización, deben cumplirse los siguientes requisitos:

  - Es el administrador global de la organización y tiene una licencia válida de Forms.

  - El empleado cuyo formulario quiere transferir tiene una cuenta que se ha eliminado o deshabilitado.

  - El formulario se transfiere dentro de los 30 días posteriores a la eliminación de una cuenta.

> [!Note]
> No hay ninguna restricción de tiempo para transferir la propiedad de un formulario desde una cuenta que se ha deshabilitado (y no eliminado).

1. Si se cumplen todos los requisitos, puede transferir la propiedad del formulario. En la barra de direcciones del explorador, reemplace la dirección URL existente por lo siguiente:

    `https://forms.office.com/Pages/delegatepage.aspx? originalowner=\[*email address*\]`

   >[!Note]
   >*correo electrónico de usuario* = dirección de correo electrónico del propietario del formulario que ha dejado la organización o cuya cuenta se ha deshabilitado.
   > Por ejemplo, si el propietario del formulario ("Jason Fabian") abandonó su organización ("Contoso"), la dirección URL de la solución alternativa tendría el siguiente aspecto: `https://forms.office.com/Pages/delegatepage.aspx?originalowner=JasonFabian@contoso.com`

2. Ahora tiene acceso a los formularios del antiguo empleado. En el formulario que quiere transferir, haga clic en **Más acciones del formulario**![botón Más opciones](./media/image2.png) y seleccione **Mover**.

   >[!Note]
   >Si intenta transferir la propiedad del formulario a un empleado activo de su organización, puede moverlo a un grupo al que pertenezca. Si aún no es miembro de ese grupo, debe unirse a él para realizar la transferencia. Una vez completada la transferencia de propiedad del formulario, puede optar por abandonar el grupo.

**Cuando intento transferir la propiedad de un formulario, ¿por qué aparece un error?**

Si recibe un mensaje de error, cualquiera de las siguientes acciones puede impedirle transferir la propiedad:

|Mensaje de error|Explicación|
| --- | --- |
| ***No podemos acceder a esta página***<br/><br/>El propietario del formulario todavía tiene una cuenta activa. | El propietario del formulario sigue teniendo una licencia y una cuenta de Forms activas. |
| ***No podemos acceder a esta página***<br/><br/>Asegúrese de que ha escrito la dirección de correo electrónico correctamente y de que la cuenta del propietario del formulario no se eliminó hace más de 30 días. | La dirección de correo electrónico está escrita incorrectamente o la cuenta del propietario del formulario se eliminó hace más de 30 días. |
| ***No podemos acceder a esta página***<br/><br/>Asegúrese de que ha escrito la dirección de correo electrónico correctamente e inténtelo de nuevo. | Falta la dirección de correo electrónico o está mal escrita. |

## <a name="forms-usage-in-outlook-or-powerpoint"></a>Uso de formularios en Outlook o PowerPoint

**La gente de mi organización no puede agregar un sondeo a un mensaje de correo electrónico de Outlook. ¿Cómo puedo corregir esto?**

La configuración de **Autenticación moderna** para Outlook debe estar habilitada para garantizar que los usuarios de su organización puedan [crear un sondeo en Outlook](https://support.microsoft.com/office/create-a-poll-in-outlook-46893563-ab12-4bd0-aff7-26f5a488fea0).

1. Inicie sesión en [https://admin.microsoft.com](https://admin.microsoft.com/) con su cuenta profesional o educativa.

2. Seleccione **Configuración** \> **Configuración de la organización**.

   >[!Note]
   > Si no ve la opción **Configuración**, seleccione el ![botón Más opciones ](./media/image2.png)**Mostrar todo** en el panel izquierdo.

3.  Seleccione **Autenticación moderna**.

4.  Active la opción **Activar la autenticación moderna para Outlook 2013 para Windows y versiones posteriores (recomendado)**.

Obtenga más información sobre la autenticación moderna y [multifactor ](/microsoft-365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)y cómo configurarla e implementarla en su organización.

**No quiero implementar complementos de Office para toda la organización. ¿Los usuarios de mi organización pueden seguir usando el complemento de Forms para PowerPoint?**

Sí, puede usar la [implementación centralizada](/office/dev/add-ins/publish/centralized-deployment) para implementar solo el complemento de Forms para PowerPoint.

1.  Inicie sesión en [https://admin.microsoft.com](https://admin.microsoft.com/) con su cuenta profesional o educativa.

2.  Seleccione **Configuración** \> **Complementos**.

    >[!Note]
    >Si no ve la opción **Configuración**, seleccione el ![botón Más opciones ](./media/image2.png)**Mostrar todo** en el panel izquierdo.

3.  En la lista **Complementos,** seleccione **Forms.**

4.  En **Asignar usuarios** en el panel **Editar Forms**, seleccione **Todos.**

5.  Seleccione **Guardar**.


## <a name="forms-and-anti-phishing"></a>Forms y protección contra la suplantación de identidad (phishing)

**¿Qué puedo hacer con la suplantación de identidad (phishing) y la posible intención malintencionada en formularios dentro de mi inquilino?**

En Microsoft Forms permitimos que las revisiones automáticas de máquinas detecten proactivamente la recopilación malintencionada de los datos confidenciales de formularios y bloqueen temporalmente la recopilación de respuestas.

Obtenga más información sobre [Microsoft Forms y la prevención proactiva de suplantación de identidad (phishing)](https://support.microsoft.com/office/microsoft-forms-and-proactive-phishing-prevention-b3950a20-296d-4e8e-96f5-594ced998a90).

Si es un administrador global o de seguridad, puede iniciar sesión en el Centro de administración de Microsoft 365 en [admin.microsoft.com](https://admin.microsoft.com/) e ir al [Centro de mensajes](https://admin.microsoft.com/AdminPortal/Home#/MessageCenter). Aquí, obtendrá un resumen diario de todos los formularios bloqueados. Para cada formulario enumerado, puede elegir si quiere desbloquearlo o confirmar su intento de suplantación de identidad (phishing). Obtenga más información sobre cómo [Revisar y desbloquear formularios o usuarios detectados y bloqueados por potencial suplantación de identidad (phishing)](review-unblock-forms-users-detected-blocked-potential-phishing.md).
