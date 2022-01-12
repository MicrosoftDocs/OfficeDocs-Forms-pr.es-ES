---
title: Configurar MicrosoftForms
ms.author: jokay
author: dumptruckjon
manager: kathyl
audience: Admin
ms.topic: how-to
ms.service: microsoft-365-education
ms.localizationpriority: high
description: Descubra cómo los administradores de Microsoft365 pueden controlar cómo se usa MicrosoftForms en su organización. Obtenga respuestas a preguntas de seguridad y cumplimiento, p. ej., dónde se almacenan los datos de MicrosoftForms.
ms.openlocfilehash: bb0e1a6ba8e2085550eb18a8bb393b34b197fe51
ms.sourcegitcommit: 80aa5565b4008855be844e8e5ab3f2779fba9a83
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/05/2022
ms.locfileid: "61723728"
---
# <a name="set-up-microsoft-forms"></a>Configurar MicrosoftForms

## <a name="overview"></a>Información general

MicrosoftForms permite a los usuarios, entre otras cosas, crear encuestas, registros y cuestionarios personalizados de forma rápida y sencilla. Al crear un cuestionario o un formulario, puede invitar a otros a que lo respondan desde cualquier navegador web o incluso desde dispositivos móviles. Cuando se envían los resultados, puede usar su sistema de análisis integrado para evaluar las respuestas. Los datos de formulario, como los resultados de cuestionarios, pueden exportarse fácilmente a Excel para un análisis adicional o para calificarlos.

Para obtener más información, vea [¿Qué es MicrosoftForms?](https://support.microsoft.com/office/what-is-microsoft-forms-6b391205-523c-45d2-b53a-fc10b22017c8) O bien, vea nuestro [blog de Microsoft365 sobre](https://go.microsoft.com/fwlink/?linkid=852256) MicrosoftForms.

>[!Note]
>MicrosoftForms está disponible con carácter general para clientes de Office365 Educación, clientes de Aplicaciones de Microsoft365 para negocios y clientes con una cuenta de Microsoft (Hotmail, Live o Outlook.com).

:::image type="content" source="./media/set-up-forms-team-event.png" alt-text="Vista previa de cómo será un formulario en un dispositivo móvil.":::

## <a name="configure"></a>Configurar

Los administradores de Microsoft365 pueden controlar cómo se usa MicrosoftForms en su organización con las siguientes tareas:

|Tarea de administración   |Descripción   |
|----------|-----------|
|**Activar o desactivar MicrosoftForms**|MicrosoftForms se activa en su organización de forma predeterminada. Puede [desactivarlo](turn-off-turn-on-microsoft-forms.md) cuando lo desee.|
|**Desactivar MicrosoftForms para personas individuales de la organización**|Si desactiva MicrosoftForms para una persona específica, esta no podrá usar *Forms* y el icono de Forms no se mostrará en su página principal ni en el iniciador de aplicaciones de Microsoft365. Obtenga información sobre [cómo desactivar formularios para personas específicas](turn-off-turn-on-microsoft-forms.md).|
|**Configurar el acceso condicional de AzureActiveDirectory condicional para MicrosoftForms**|Para configurar una directiva de acceso condicional para MicrosoftForms, consulte la [documentación de AzureAD sobre el acceso condicional](/azure/active-directory/conditional-access) e incluya *Microsoft Forms* en las asignaciones de *aplicaciones en la nube.* <br/><br/> **Nota:** Si los usuarios de la organización siguen bloqueados incluso después de configurar el acceso condicional para MicrosoftForms, asegúrese de que también se les haya concedido acceso a SharePointOnline y ExchangeOnline a través del acceso condicional. [Más información](/azure/active-directory/conditional-access/block-legacy-authentication).|
|**Controlar la configuración de uso compartido externo, registrar nombres de personas de su organización o proteger formularios contra la suplantación de identidad (phishing)**|En el Centro de administración de Microsoft365, puede: <ul><li>Decidir si los usuarios externos tienen la opción de colaborar con usuarios de su organización en un formulario o cuestionario.</li><li>Elegir si desea capturar o no los nombres de las personas de su organización que rellenan formularios.</li><li>Desactivar o activar la detección automática de suplantación de identidad en formularios.</li></ul><br/>Obtenga más información sobre esta [configuración de administración.](administrator-settings-microsoft-forms.md)|
|**Permitir a los usuarios insertar un formulario en PowerPoint**|<ol><li>Inicie sesión en https://admin.microsoft.com.</li><li>Haga clic en **Configuración** > **Configuración**.</li><li>En la página **Configuración,** en la pestaña **Servicios**, haga clic en **Aplicaciones y servicios de propiedad del usuario.**</li><li>Active la opción **Permitir que los usuarios accedan** a Office para permitirles insertar un formulario en PowerPoint.</li></ol><br/>Tenga en cuenta que el cambio puede tardar unas horas en surtir efecto. [Más información](/microsoft-365/admin/manage/manage-deployment-of-add-ins)|

## <a name="security--compliance"></a>Seguridad y cumplimiento

Si su empresa tiene que cumplir estándares técnicos, normativos y legales relacionados con la seguridad del contenido y el uso de los datos, se encuentra en la sección adecuada.

**¿Dónde se almacenan los datos de MicrosoftForms?**

Los datos de MicrosoftForms se almacenan en servidores de Estados Unidos y Europa. Todos los datos se encuentran en Estados Unidos, excepto los de aquellos inquilinos basados en Europa que empezaron a usar MicrosoftForms después de mayo de 2017. Sus datos se almacenan en bases de datos de Europa.

**¿Cumple MicrosoftForms la normativa legal?**

MicrosoftForms cumple los requisitos normativos del RGPD desde mayo de 2018. Para más información, consulte [Solicitudes de los interesados de Microsoft365 para el RGPD](/microsoft-365/compliance/gdpr-dsr-office365?toc=/microsoft-365/enterprise/toc.json).

**¿Están establecidas las protecciones FERPA y BAA?**

MicrosoftForms cumple los estándares de protección [FERPA](https://www.microsoft.com/trustcenter/compliance/ferpa) y [BAA](https://www.microsoft.com/TrustCenter/Compliance/HIPAA).

**¿Existe un límite en el número de usuarios y en la cantidad de datos que se almacenan para las cuentas de usuario incluso después de que hayan dejado la organización?**

De momento, no existe un límite de usuarios para los que se conservan los datos, siempre que el aprovisionamiento de sus cuentas esté dentro del contrato de servicio en línea de la organización. Tampoco existe un límite de cantidad de datos almacenados para cuentas de usuario.

**El propietario original de un formulario ya no está en la organización o su licencia de MicrosoftForms se ha quitado. ¿Qué sucede con los datos asociados con el formulario que ha creado?**

Todos los datos relacionados con la cuenta se eliminarán 30 días después de que se haya eliminado la cuenta de usuario del inquilino (AzureAD).

## <a name="faq"></a>Preguntas más frecuentes

**¿Para qué puedo usar MicrosoftForms?**

MicrosoftForms es una aplicación sencilla y ligera que le permite crear fácilmente encuestas, cuestionarios y sondeos. En las instituciones educativas, se puede usar para crear cuestionarios, recopilar comentarios de profesores y padres, o planear actividades de clase o para el personal docente. En organizaciones empresariales, se puede usar para recopilar comentarios de los clientes, medir la satisfacción de los empleados, mejorar su producto o negocio u organizar eventos de empresa.

**¿Quién Puede usar MicrosoftForms?**

MicrosoftForms es gratuito para cualquier persona con una cuenta de Microsoft (Hotmail, Live o Outlook.com). Los siguientes clientes de Office365 Educación y Aplicaciones de Microsoft365 para negocios también pueden usar MicrosoftForms:

**Office 365 Educación**

  - Office365 A1 Plus

  - Office 365 A5

  - Clientes existentes que compraron Microsoft Office365 para el ámbito educativo E3 antes de su retirada

**Aplicaciones de Microsoft 365 para negocios**

  - Microsoft 365 Empresa Básico

  - Microsoft 365 Empresa Estándar

  - Microsoft 365 Empresa Premium

  - Aplicaciones de Microsoft 365 para empresas

  - Microsoft365 Enterprise con los planes E1, E3 y E5

  - Clientes de Office365 Enterprise E4 que compraron E4 antes de su retirada

Inicie sesión en [forms.office.com](https://forms.office.com/) y comience a crear encuestas, cuestionarios y sondeos.

**¿Pueden las personas sin una cuenta de Microsoft365 enviar una encuesta o un cuestionario en MicrosoftForms?**

Los autores de MicrosoftForms pueden alternar su configuración para permitir que los usuarios fuera de su organización respondan a su encuesta o cuestionario. En este caso, los usuarios enviarán respuestas de forma anónima. Si quieres ver quién ha completado la encuesta o el cuestionario, puedes requerir a los encuestados que escriban sus nombres como parte del cuestionario.

**¿Cuántos formularios se pueden crear como máximo y cuál es el límite de respuestas para un formulario?**

Los clientes de Office365Educación y Aplicaciones de Microsoft365 para negocios pueden crear hasta 200 formularios y cada formulario puede recibir hasta 50 000 respuestas. Los usuarios de MicrosoftForms con una cuenta de Microsoft (Hotmail, Live o Outlook.com) pueden crear hasta 200formularios y cada formulario puede recibir hasta 1000respuestas para cuentas de pago y hasta 200 respuestas para cuentas gratuitas. Obtenga más información sobre los [límites de formularios, preguntas, respuestas y caracteres en Forms.](https://support.microsoft.com/office/form-question-response-and-character-limits-in-microsoft-forms-ec15323d-92a4-4c33-bf88-3fdb9e5b5fea)

Si necesita más respuestas, le recomendamos exportar las respuestas existentes a un libro de Excel y, a continuación, borrarlas de la encuesta o cuestionario. Esto le permitirá recopilar más respuestas una vez desactivadas.

**¿Con qué exploradores web funciona MicrosoftForms?**

MicrosoftForms está optimizado para funcionar con Internet Explorer 11, Edge, Chrome (versión más reciente), Firefox (versión más reciente), Chrome en Android (versión más reciente) y Safari en iOS (versión más reciente).

**¿En qué idiomas está disponible MicrosoftForms?**

Consulta [Idiomas admitidos](https://support.microsoft.com/office/languages-supported-by-microsoft-forms-c17498cb-cbf6-4178-ae83-bd24934398ac) y [configuración de idioma](https://support.microsoft.com/office/language-settings-for-microsoft-forms-b282f9aa-0fe4-4290-b1e1-827a8a35ac27) para MicrosoftForms.

**¿Reemplazará MicrosoftForms a Microsoft InfoPath?**

No. MicrosoftInfoPath era una solución para crear formularios personalizables que podían habilitar flujos de trabajo automatizados, mientras que MicrosoftForms es una aplicación básica y ligera para recopilar información rápidamente a través de encuestas y cuestionarios.

Estamos reemplazando MicrosoftInfoPath con SharePointLists, Flow y PowerApps: soluciones modernas para digitalizar formularios de empresa tradicionales, automatizar flujos de trabajo y transformar procesos empresariales. [Más información](https://products.office.com/business/business-process-automation).

**¿Desde dónde puedo enviar comentarios como errores de producto o solicitudes de características?**

Queremos conocer su opinión. Para enviar comentarios sobre MicrosoftForms, vaya a la esquina superior derecha del formulario y seleccione **Más opciones del formulario** ![Botón Más opciones](./media/image2.png) >  **Comentarios**.

> [!Note]
> Consulte [Preguntas más frecuentes sobre MicrosoftForms](https://support.microsoft.com/office/frequently-asked-questions-about-microsoft-forms-495c4242-6102-40a0-add8-df05ed6af61c) para obtener más información.

