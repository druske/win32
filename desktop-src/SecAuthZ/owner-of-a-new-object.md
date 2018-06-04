---
Description: 'An object's owner implicitly has WRITE\_DAC access to the object. This means that the owner can modify the object's discretionary access control list (DACL), and thus, can control access to the object.'
ms.assetid: '16144f38-3416-4594-b5e4-ca84fcbdddc9'
title: Owner of a New Object
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Owner of a New Object

An object's owner implicitly has WRITE\_DAC access to the object. This means that the owner can modify the object's [*discretionary access control list*](https://msdn.microsoft.com/library/windows/desktop/ms721573#-security-discretionary-access-control-list-gly) (DACL), and thus, can control access to the object.

The owner of a new object is the default owner [*security identifier*](https://msdn.microsoft.com/library/windows/desktop/ms721625#-security-security-identifier-gly) (SID) from the [*primary*](https://msdn.microsoft.com/library/windows/desktop/ms721603#-security-primary-token-gly) or [*impersonation token*](https://msdn.microsoft.com/library/windows/desktop/ms721588#-security-impersonation-token-gly) of the creating [*process*](https://msdn.microsoft.com/library/windows/desktop/ms721603#-security-process-gly). To get or set the default owner in an [*access token*](https://msdn.microsoft.com/library/windows/desktop/ms721532#-security-access-token-gly), call the [**GetTokenInformation**](https://www.bing.com/search?q=**GetTokenInformation**) or [**SetTokenInformation**](https://www.bing.com/search?q=**SetTokenInformation**) function with the [**TOKEN\_OWNER**](/windows/desktop/api/Winnt/ns-winnt-_token_owner) structure. The system does not allow you to set a token's default owner to a SID that is not valid, such as the SID of another user's account.

A process with the SE\_TAKE\_OWNERSHIP privilege enabled can set itself as the owner of an object. A process with the SE\_RESTORE\_NAME privilege enabled or with WRITE\_OWNER access to the object can set any valid user or group SID as the owner of an object.

 

 


