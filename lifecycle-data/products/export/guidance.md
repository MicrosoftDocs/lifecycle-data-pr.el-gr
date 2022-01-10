---
title: Οδηγίες εξαγωγής δεδομένων κύκλου ζωής
description: Οδηγίες εξαγωγής πληροφοριών κύκλου ζωής προϊόντος
ms.date: 12/16/2020
layout: ContentPage
ms.openlocfilehash: 5e9dddbff5fac32e6d3cf8ef0943151d2dfe5e35
ms.sourcegitcommit: 6ea3221fd5475440480515f04f33988656d71748
ms.translationtype: HT
ms.contentlocale: el-GR
ms.lasthandoff: 11/02/2021
ms.locfileid: "3546799"
---
# <a name="lifecycle-data-export-guidance"></a>Οδηγίες εξαγωγής δεδομένων κύκλου ζωής
Αυτό το έγγραφο περιγράφει τον τρόπο χρήσης του αρχείου εξαγωγής προϊόντος.

## <a name="query-information"></a>Πληροφορίες ερωτημάτων
Στο έγγραφο Excel, υπάρχουν πεδία που θα σας βοηθήσουν να εντοπίσετε τα δεδομένα που έχουν συμπληρωθεί στον πίνακα προϊόντος.

### <a name="end-of-support"></a>Λήξη της υποστήριξης
Η τιμή λήξης της υποστήριξης θα φιλτράρει τα προϊόντα είτε με βάση την ημερομηνία λήξης της υποστήριξης των προϊόντων είτε με βάση τις ημερομηνίες λήξης της κυκλοφορίας τους.

Πιθανές τιμές: Όλα (δεν εφαρμόζεται φίλτρο), Έτος και Εύρος.

### <a name="family"></a>Οικογένεια
Η τιμή "Οικογένεια" φιλτράρει τα προϊόντα με βάση το γονικό τους επίπεδο εντός της ιεραρχίας που είναι γνωστή ως η οικογένεια.

Πιθανές τιμές: Όλα (δεν εφαρμόζεται φίλτρο), Όνομα οικογένειας

### <a name="group"></a>Ομάδα
Η τιμή "Ομάδα" φιλτράρει τα προϊόντα εντός του γονικού τους επιπέδου (οικογένεια) σε μια συγκεκριμένη ομάδα.

Πιθανές τιμές: Όλα (δεν εφαρμόζεται φίλτρο), Όνομα ομάδας

## <a name="table-columns"></a>Στήλες πίνακα
Ο πίνακας προϊόντος αποτελείται από στήλες που ορίζουν το προϊόν, τις εκδόσεις, τις κυκλοφορίες και τις αντίστοιχες ημερομηνίες υποστήριξης.

> [!NOTE]
> Θα υπάρχει μια γραμμή για κάθε προϊόν, έκδοση και συνδυασμό κυκλοφορίας.

### <a name="product"></a>Προϊόν
Το όνομα του προϊόντος.

### <a name="edition"></a>Έκδοση (Edition)
Η στήλη "Έκδοση" θα συμπληρώνεται όταν το προϊόν περιέχει εκδόσεις. Όταν δεν υπάρχει έκδοση προϊόντος, αυτό το πεδίο θα είναι κενό.

### <a name="release"></a>Έκδοση
Η στήλη "Κυκλοφορία" θα συμπληρώνεται όταν το προϊόν περιέχει πολλές κυκλοφορίες.
Όταν το προϊόν έχει μόνο μία κυκλοφορία, αυτό το πεδίο θα είναι κενό.

### <a name="support-policy"></a>Πολιτική υποστήριξης
Αυτό το πεδίο καθορίζει ποια πολιτική υποστήριξης ακολουθεί το προϊόν.

Πιθανές τιμές: [Σταθερή,](/lifecycle/policies/fixed) [Σύγχρονη](/lifecycle/policies/modern), Σύνθετη

### <a name="start-date"></a>Ημερομηνία έναρξης
Ημερομηνία έναρξης υποστήριξης για το προϊόν.

### <a name="mainstream-date"></a>Βασική ημερομηνία
Όταν η Πολιτική υποστήριξης είναι **Σταθερή** ή **Σύνθετη**, αυτή είναι η βασική ημερομηνία λήξης του προϊόντος.
  
Όταν η Πολιτική υποστήριξης είναι **Σύγχρονη**, αυτή η επιλογή θα είναι κενή.

### <a name="extended-end-date"></a>Εκτεταμένη ημερομηνία λήξης
Όταν η Πολιτική υποστήριξης είναι **Σταθερή** ή **Σύνθετη**, αυτή είναι η ημερομηνία λήξης της εκτεταμένης ημερομηνίας του προϊόντος.

Όταν η Πολιτική υποστήριξης είναι **Σύγχρονη**, αυτή η επιλογή θα είναι κενή.

### <a name="retirement-date"></a>Ημερομηνία απόσυρσης
Όταν η Πολιτική υποστήριξης είναι **Σταθερή** ή **Σύνθετη**, αυτή η επιλογή θα είναι κενή.

Όταν η Πολιτική υποστήριξης είναι **Σύγχρονη**, αυτή θα είναι η ημερομηνία απόσυρσης του προϊόντος.

### <a name="release-start-date"></a>Ημερομηνία έναρξης κυκλοφορίας
Ημερομηνία έναρξης υποστήριξης για την κυκλοφορία. Όταν το προϊόν έχει μόνο μία κυκλοφορία, αυτό το πεδίο θα είναι κενό.
 
### <a name="release-end-date"></a>Ημερομηνία λήξης κυκλοφορίας
Ημερομηνία λήξης υποστήριξης για την κυκλοφορία.
Όταν το προϊόν έχει μόνο μία κυκλοφορία, αυτό το πεδίο θα είναι κενό.

### <a name="docs-url"></a>Docs Url
Διεύθυνση Url για εκτεταμένη τεκμηρίωση.