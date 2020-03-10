---
layout: statement
codename: telecom
---

Μια τηλεπικοινωνιακή εταιρεία προσπαθεί να προσελκύσει ένα νέο πελάτη. Ο πελάτης ενδιαφέρεται για την ενοικίαση οπτικών ινών που εξασφαλίζουν τη διασύνδεση $$N$$ πόλεων $$a_1, a_2, \ldots , a_N$$. Η εταιρεία πρέπει να καταθέσει προσφορά με το κόστος $$c_{ij}$$ για την απευθείας σύνδεση κάθε ζεύγους πόλεων $$a_i$$ και $$a_j$$, $$1 \leq i, j \leq N$$, με $$i\neq j$$. Με βάση την προσφορά, ο πελάτης θα επιλέξει ένα συνδετικό δέντρο (spanning tree) που να καλύπτει όλες τις πόλεις και να εξασφαλίζει ελάχιστο συνολικό κόστος σύνδεσης.

Η εταιρεία έχει σημαντικούς λόγους να χειραγωγήσει την επιλογή του πελάτη, οδηγώντας τον στην επιλογή ενός συγκεκριμένου συνδετικού δέντρου $$T$$ για τη διασύνδεση των πόλεων. Με δεδομένο το κόστος των συνδέσεων που εντάσσονται στο $$T$$, η εταιρεία επιθυμεί να προσαρμόσει το κόστος των υπόλοιπων συνδέσεων ώστε το δέντρο $$T$$ να προκύπτει ως το μοναδικό ελάχιστο συνδετικό δέντρο που καλύπτει όλες τις πόλεις. Όμως, για να μην φανεί στον πελάτη ότι η προσφορά είναι πολύ ακριβή, η εταιρεία επιθυμεί το προτεινόμενο κόστος για τις υπόλοιπες συνδέσεις να υπολογισθεί ώστε το συνολικό άθροισμα του προτεινόμενου κόστους για όλα τα ζεύγη πόλεων να είναι το ελάχιστο δυνατό.

## Πρόβλημα

Nα αναπτύξετε ένα πρόγραμμα σε μια από τις γλώσσες του ΙΟΙ το οποίο: αφού διαβάσει τα κόστη των συνδέσεων που εντάσσονται στο συνδετικό δέντρο $$T$$, θα υπολογίζει το ελάχιστο δυνατό συνολικό προτεινόμενο κόστος στην προσφορά της εταιρείας, έτσι ώστε το $$T$$ να είναι το μοναδικό ελάχιστο συνδετικό δέντρο.


## Aρχεία εισόδου

Tα αρχεία εισόδου, με όνομα **telecom.in**, είναι αρχεία κειμένου με την εξής δομή: Στην πρώτη γραμμή έχουν έναν ακέραιο αριθμό $$N$$ ($$3 \leq N \leq 500.000$$), το πλήθος των πόλεων. Οι πόλεις αριθμούνται από $$1$$ έως $$N$$. Σε κάθε μία από τις επόμενες $$N−1$$ γραμμές θα υπάρχουν τρεις θετικοί ακέραιοι $$i$$, $$j$$, και $$c_{ij}$$, χωρισμένοι ανά δύο με ένα κενό διάστημα. Αυτοί δηλώνουν ότι η πόλη ai συνδέεται απευθείας στο επιλεγμένο δέντρο $$T$$ με την πόλη $$a_j$$ με κόστος $$c_{ij}$$. Θα ισχύει $$1 \leq i, j \leq N$$, $$i\neq j$$ και $$1 \leq c_{ij} \leq 12.000$$.

## Aρχεία εξόδου

Tα αρχεία εξόδου με το όνομα **telecom.out** είναι αρχεία κειμένου με την εξής δομή: Θα περιέχουν μία μόνο γραμμή με έναν μόνο ακέραιο αριθμό, το ελάχιστο συνολικό προτεινόμενο κόστος για όλα τα ζεύγη πόλεων, έτσι ώστε το επιλεγμένο δέντρο $$T$$ να αποτελεί το μοναδικό ελάχιστο συνδετικό δέντρο για τις πόλεις $$a_1, a_2, \ldots , a_N$$ με βάση τα προτεινόμενα κόστη.

**Προσοχή:** Για μεγάλες τιμές του $$N$$, το ελάχιστο συνολικό κόστος (και ίσως κάποια από τα ενδιάμεσα αποτελέσματα που χρειάζονται για τον υπολογισμό του) μπορεί να υπερβαίνουν το $$2^{32}$$.

## Παραδείγματα αρχείων εισόδου - εξόδου

**1<sup>o</sup>:**

| **telecom.in**                         | **telecom.out** |
| ------------------------------------ | ------------- |
| 3 <br> 1 2 4 <br> 2 3 7 | 19 |

*Εξήγηση:* Tο επιλεγμένο δέντρο έχει απευθείας συνδέσεις μεταξύ των πόλεων $$1$$ και $$2$$, με κόστος $$4$$, και των πόλεων $$2$$ και $$3$$, με κόστος $$7$$. Για να είναι αυτό το μοναδικό ελάχιστο συνδετικό δέντρο μεταξύ των πόλεων $$1$$, $$2$$, και $$3$$, πρέπει το προτεινόμενο κόστος για τη σύνδεση των πόλεων $$1$$ και $$3$$ να είναι τουλάχιστον $$8$$. Άρα το ελάχιστο συνολικό προτεινόμενο κόστος είναι ίσο με $$4+7+8 = 19$$.

**2<sup>o</sup>:**

| **telecom.in**                         | **telecom.out** |
| ------------------------------------ | ------------- |
| 4 <br> 1 2 1 <br> 1 3 1 <br> 1 4 2 | 12 |

*Εξήγηση:* Tο επιλεγμένο δέντρο έχει απευθείας συνδέσεις μεταξύ των πόλεων $$1$$ και $$2$$, με κόστος $$1$$, των πόλεων $$1$$ και $$3$$, με κόστος $$1$$, και των πόλεων $$1$$ και $$4$$, με κόστος $$2$$. Για να είναι αυτό το μοναδικό ελάχιστο συνδετικό δέντρο μεταξύ των πόλεων $$1$$, $$2$$, $$3$$ και $$4$$, πρέπει το προτεινόμενο κόστος για τη σύνδεση των πόλεων $$2$$ και $$3$$ να είναι τουλάχιστον $$2$$, για τη σύνδεση των πόλεων $$2$$ και $$4$$, το κόστος πρέπει να είναι τουλάχιστον $$3$$, και για τη σύνδεση των πόλεων $$3$$ και $$4$$, το κόστος πρέπει να είναι τουλάχιστον $$3$$. Άρα το ελάχιστο συνολικό προτεινόμενο κόστος είναι ίσο με $$1+1+2+2+3+3 = 12$$.


**Mορφοποίηση:** Στην έξοδο, όλες οι γραμμές τερματίζουν με ένα χαρακτήρα newline. <br>
**Mέγιστος χρόνος εκτέλεσης:** $$1$$ sec. <br>
**Mέγιστη διαθέσιμη μνήμη:** $$64$$ MB.