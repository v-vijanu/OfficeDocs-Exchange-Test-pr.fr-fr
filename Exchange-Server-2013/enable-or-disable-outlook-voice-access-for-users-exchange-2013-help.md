﻿---
title: 'Activer ou désactiver Outlook Voice Access pour les utilisateurs: Exchange 2013 Help'
TOCTitle: Activer ou désactiver Outlook Voice Access pour les utilisateurs
ms:assetid: c0c244a0-ad2f-4adf-bc1f-1d55fd7ea2d5
ms:mtpsurl: https://technet.microsoft.com/fr-fr/library/Dd351106(v=EXCHG.150)
ms:contentKeyID: 52057170
ms.date: 05/23/2018
mtps_version: v=EXCHG.150
ms.translationtype: MT
---

# Activer ou désactiver Outlook Voice Access pour les utilisateurs

 

_**Sapplique à :**Exchange Online, Exchange Server 2013, Exchange Server 2016_

_**Dernière rubrique modifiée :**2012-12-12_

Vous pouvez activer ou désactiver l'accès à Outlook Voice Access pour les utilisateurs à extension messagerie unifiée associés à une stratégie de boîte aux lettres de messagerie unifiée. Outlook Voice Access est une fonctionnalité utilisée par les utilisateurs à extension messagerie unifiée pour accéder à leur boîte aux lettres sur un téléphone. Par défaut, ce paramètre est activé.

Pour les autres tâches de gestion relatives aux stratégies de boîte aux lettres de messagerie unifiée, consultez la rubrique [Procédures de stratégie de boîte aux lettres de messagerie unifiée](um-mailbox-policy-procedures-exchange-2013-help.md).

## Ce qu'il faut savoir avant de commencer

  - Durée d'exécution estimée : 2 minutes.

  - Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Stratégies de boîte aux lettres de messagerie unifiée » dans la rubrique [Autorisations de messagerie unifiée](unified-messaging-permissions-exchange-2013-help.md).

  - Avant d'exécuter ces procédures, vérifiez qu'un plan de numérotation de messagerie unifiée a été créé. Pour obtenir la procédure détaillée, consultez la rubrique [Créer un plan de numérotation de messagerie unifiée](create-a-um-dial-plan-exchange-2013-help.md).

  - Avant d'effectuer ces procédures, vérifiez qu'une stratégie de boîte aux lettres de messagerie unifiée a été créée. Pour obtenir la procédure détaillée, consultez la rubrique [Créer une stratégie de boîte aux lettres de messagerie unifiée](create-a-um-mailbox-policy-exchange-2013-help.md).

  - Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013[Raccourcis clavier dans le Centre d’administration Exchange](keyboard-shortcuts-in-the-exchange-admin-center-exchange-online-protection-help.md).

<table>
<thead>
<tr class="header">
<th><img src="images/Bb125224.tip(EXCHG.150).gif" title="Conseil" alt="Conseil" />Conseil :</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vous rencontrez des difficultés ? Demandez de l’aide en participant aux forums Exchange. Visitez les forums sur les pages <a href="https://go.microsoft.com/fwlink/p/?linkid=60612">Exchange Server</a>, <a href="https://go.microsoft.com/fwlink/p/?linkid=267542">Exchange Online</a>, et <a href="https://go.microsoft.com/fwlink/p/?linkid=285351">Exchange Online Protection</a>..</td>
</tr>
</tbody>
</table>


## Que souhaitez-vous faire ?

## Utiliser le Centre d'administration Exchange (CAE) pour activer ou désactiver Outlook Voice Access

1.  Dans le CAE, accédez à **Messagerie unifiée** \> **Plans de numérotation de messagerie unifiée**. Dans l'affichage Liste, sélectionnez le plan de numérotation de messagerie unifiée à modifier puis cliquez sur **Modifier**![Icône Modifier](images/Bb124582.6f53ccb2-1f13-4c02-bea0-30690e6ea71d(EXCHG.150).gif "Icône Modifier").

2.  Sous **Stratégies de boîte aux lettres de messagerie unifiée**, sélectionnez la stratégie de boîte aux lettres de messagerie unifiée à gérer, puis cliquez sur **Modifier**![Icône Modifier](images/Bb124582.6f53ccb2-1f13-4c02-bea0-30690e6ea71d(EXCHG.150).gif "Icône Modifier").

3.  Dans la page **Stratégie de boîte aux lettres de messagerie unifiée**, cochez ou décochez la case en regard de **Autoriser Outlook Voice Access**.

4.  Cliquez sur **Enregistrer**.

## Utiliser l'environnement de ligne de commande Exchange Management Shell pour activer ou désactiver Outlook Voice Access

Cet exemple permet aux utilisateurs associés à la stratégie de boîte aux lettres de messagerie unifiée `MyUMMailboxPolicy` d'utiliser Outlook Voice Access.

    Set-UMMailboxPolicy -identity MyUMMailboxPolicy -AllowSubscriberAccess $true

Cet exemple empêche les utilisateurs associés à la stratégie de boîte aux lettres de messagerie unifiée `MyUMMailboxPolicy` d'utiliser Outlook Voice Access.

    Set-UMMailboxPolicy -identity MyUMMailboxPolicy -AllowSubscriberAccess $false
