---
title: Revisar y desbloquear formularios o usuarios detectados y bloqueados por potencial suplantación de identidad (phishing)
ms.author: jokay
author: dumptruckjon
manager: kathyl
audience: Admin
ms.topic: how-to
ms.service: forms-pro
ms.localizationpriority: high
description: Microsoft Forms permite las revisiones automáticas de máquinas para detectar de manera proactiva la recopilación de datos confidenciales malintencionados en formularios y encuestas. Si es un administrador global o de seguridad, puede iniciar sesión en el Centro de administración de Microsoft 365 para revisar y desbloquear los formularios detectados y bloqueados debido a posibles intentos malintencionados y de suplantación de identidad.
ms.openlocfilehash: dd4b92c09393db4c81ac5e7711ee7331ac35558e
ms.sourcegitcommit: 09bdc82ce67e74495b6c58d9c842e31c17956fc3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2021
ms.locfileid: "60951579"
---
# <a name="review-and-unblock-forms-or-users-detected-and-blocked-for-potential-phishing"></a>Revisar y desbloquear formularios o usuarios detectados y bloqueados por potencial suplantación de identidad (phishing)

Microsoft Forms permite que las revisiones automáticas de máquinas detecten proactivamente la colección malintencionada de los datos confidenciales de los formularios y bloqueen temporalmente la recopilación de respuestas. Obtenga más información sobre [Microsoft Forms y la prevención proactiva de suplantación de identidad (phishing)](https://support.microsoft.com/office/microsoft-forms-and-proactive-phishing-prevention-b3950a20-296d-4e8e-96f5-594ced998a90).

>[!Note]
>Los pasos de este documento también se aplican a [Dynamics 365 Customer Voice](https://go.microsoft.com/fwlink/p?linkid=2128500) (anteriormente conocido como Forms Pro). Tenga en cuenta que se requiere una licencia de Dynamics 365 Customer Voice para desbloquear las encuestas de Dynamics 365 Customer Voice. [Más información](/dynamics365/customer-voice/help-hub).

## <a name="review-alerts-in-the-microsoft-365-defender-portal"></a>Revisar alertas en el portal Microsoft 365 Defender

Si eres un administrador global o de seguridad, recibirás alertas en el portal de [Microsoft 365 Defender](https://security.microsoft.com/) sobre posibles formularios de suplantación de identidad (phishing) para los que puedes tomar medidas.

>[!Note]
> Si es un administrador global, recibirá los mensajes de privacidad de datos para su organización, incluidas las notificaciones diarias de cualquier formulario creado en el espacio empresarial que se haya detectado y bloqueado por una posible suplantación de identidad (phishing). Verá estas notificaciones en el [Centro de mensajes](https://admin.microsoft.com/AdminPortal/Home#/MessageCenter) buscando la **notificación de suplantación de identidad (phishing) de Microsoft Forms**. (Si no ve esta notificación en la pestaña o vista de **Todos los mensajes activos**, puede encontrarlo en la pestaña/vista **Mensajes descartados**). Para cada notificación, seleccione el vínculo o vínculos **Formulario del administrador de revisión de la dirección URL** para revisar los formularios bloqueados.  
  
Para que los administradores de seguridad también reciban notificaciones sobre posibles formularios de suplantación de identidad, los administradores globales deben asignarles el rol [lector de privacidad del Centro de mensajes](/azure/active-directory/roles/permissions-reference#message-center-privacy-reader). Para obtener más información sobre el Centro de mensajes, vea las [preguntas más frecuentes](/microsoft-365/admin/manage/message-center). Vea también cómo establecer las [preferencias de correo electrónico para los mensajes de privacidad de datos](/microsoft-365/admin/manage/message-center#preferences).

1.  Inicie sesión en el portal de [Microsoft 365 Defender](https://security.microsoft.com/).

2.  Seleccione **Incidencias y** \> **alertas**. Es posible que vea una o todas estas alertas para los formularios:
    
      - **El usuario no puede compartir formularios ni recopilar respuestas**
    
      - **Formulario marcado y confirmado como suplantación de identidad (phishing)**
    
      - **Formulario bloqueado debido a un posible intento de suplantación de identidad (phishing)**

3.  Seleccione una alerta para revisarla. Para revisar el formulario marcado, pulse o haga clic en los tres puntos de la esquina inferior derecha junto al botón **Administrar alerta** y, a continuación, seleccione **Revisar este formulario**.
 
    :::image type="content" source="./media/review-unblock-forms-review-this-form.png" alt-text="Revisar esta opción de formulario":::

    >[!Tip]
    >Obtenga más información sobre [las directivas de alerta en Microsoft 365](/microsoft-365/compliance/alert-policies).

## <a name="unblock-a-form-or-confirm-its-phishing-attempt"></a>Desbloquear un formulario o confirmar su intento de suplantación de identidad (phishing)

Para cada formulario que revise, puede elegir si quieresdesbloquearlo o confirmar la suplantación de identidad (phishing).

### <a name="unblock"></a>Desbloquear

Seleccione **Desbloquear** si no cree que un formulario tenga una intención malintencionada.

>[!Note]
>Si alguien de su espacio empresarial le solicita que desbloquee su formulario, le sugerimos que solicite información específica del formulario (por ejemplo, la fecha y hora de bloqueo o el título) para identificar de forma más eficaz la notificación en el centro de administración. Dado que las notificaciones se envían diariamente e incluyen todos los formularios detectados en las últimas 24 horas, la información identificable del formulario será útil.

### <a name="confirm-phishing"></a>Confirmar suplantación de identidad

Seleccione **Confirmar suplantación de identidad (phishing)** si cree que un formulario tiene una intención malintencionada. El formulario se bloqueará permanentemente y su propietario ya no podrá editarlo ni eliminarlo.

Una vez que haya seleccionado **Confirmar suplantación de identidad (phishing)**, haga clic o pulse en **Eliminar formulario** para eliminar permanentemente el formulario del espacio empresarial. Le recomendamos encarecidamente que restablezca inmediatamente la contraseña de la cuenta en su espacio empresarial que cree que se ha visto comprometida.

>[!Tip]
>La selección de **Confirmar suplantación de identidad (phishing)** ayuda a Microsoft Forms a mejorar la precisión de detección. 

## <a name="commonly-asked-questions"></a>Preguntas frecuentes

**Cuando voy a revisar un formulario bloqueado, ¿por qué no veo la opción de desbloquearlo o confirmar suplantación de identidad (phishing)?**

Al revisarlo, es posible que vea que ya se ha originado un bloqueo del formulario. Esto significa que, entre el momento en que se bloqueó el formulario y el momento en que lo revisó, el propietario del formulario quitó las palabras clave que estaban marcadas por posible suplantación de identidad (phishing). En esta situación, no es necesario realizar ninguna acción adicional.

**Si se ha bloqueado un formulario por suplantación de identidad (phishing) confirmada, ¿puedo quitarlo?**

Si el formulario ya se ha bloqueado por confirmación de suplantación de identidad (phishing), seleccione **Eliminar formulario** para quitarlo del espacio empresarial.

**¿Qué ocurre si no tomo ninguna acción en un formulario bloqueado?**

Si decide no realizar ninguna acción (ni desbloquear el formulario ni confirmar un intento de suplantación de identidad o phishing), el formulario permanecerá bloqueado. El propietario del formulario aún puede editar el formulario y quitar las palabras clave que se marcaron por posible suplantación de identidad.

**¿Qué ocurre si quiero editar o eliminar el contenido bloqueado en el formulario?**

Si prefiere editar o eliminar el contenido bloqueado, puede generar una página de coautoría y administrar el formulario como coautor. Para ello, haga clic en el vínculo **abrir una página de coautoría**, ubicada en los mensajes que hay encima del formulario que está revisando.

## <a name="remove-restrictions-for-blocked-microsoft-forms-users"></a>Quitar restricciones para los usuarios bloqueados de Microsoft Forms

Microsoft Forms bloquea a los usuarios que han intentado recopilar información personal o confidencial repetidamente para distribuir formularios y recopilar respuestas. Se notificará a los administradores globales de estos usuarios bloqueados a través del [Centro de mensajes](https://admin.microsoft.com/AdminPortal/Home#/MessageCenter). Si cree que un usuario bloqueado no tiene ninguna intención malintencionada y su cuenta es segura, puede seguir estos pasos para desbloquearlo.

>[!Note]
>Los administradores de seguridad también pueden recibir notificaciones sobre posibles formularios de suplantación de identidad (phising) una vez que un administrador global les asigna el rol [lector de privacidad del Centro de mensajes](/azure/active-directory/roles/permissions-reference#message-center-privacy-reader).

1.  Vaya al [Centro de mensajes](https://admin.microsoft.com/AdminPortal/Home#/MessageCenter) y busque la notificación **Prevenir/Solucionar: posible suplantación de identidad (phishing) detectada por Microsoft Forms**.

    >[!Note]
    >Si no ve esta notificación en la pestaña/vista **Todos los mensajes activos**, puede encontrarla en la pestaña o vista **Mensajes descartados**.
 
    Esta notificación contiene una lista de usuarios del inquilino que están bloqueados para compartir formularios y recopilar respuestas.

2.  Haga clic en el vínculo proporcionado en la notificación para revisar los usuarios bloqueados.

3.  Para cada usuario que crea que no tiene ninguna intención malintencionada, puede hacer clic en el vínculo **Desbloquear** de la columna **Acciones** asociada a ese usuario.

    >[!Note]
    >Si cree que un usuario tiene una intención malintencionada, no es necesario realizar ninguna acción adicional.

    >[!Note]
    >Se pueden tardar 30 minutos o más antes de quitar las restricciones.

