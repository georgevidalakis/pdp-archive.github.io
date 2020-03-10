---
layout: statement
codename: rafting
---

Η *κατάβαση ποταμών με σχεδία – φουσκωτή βάρκα* (rafting) είναι μία πολύ συναρπαστική και διασκεδαστική εμπειρία. Στο rafting το πλήρωμα αποτελείται από $$6$$ έως $$12$$ κωπηλάτες που κατευθύνουν τη φουσκωτή βάρκα μέσα από ποτάμια με βαθμό δυσκολίας από 1<sup>ο</sup>–7<sup>ο</sup>, ανάλογα με την ορμητικότητα των νερών και το ανάγλυφο της κοίτης. Στην Ελλάδα, δεκάδες ποταμοί μεταξύ των οποίων ο Αχέροντας, ο Βοϊδομάτης, ο Ερύμανθος, και ο Λούσιος τους χειμερινούς μήνες, γίνονται θέρετρα χειμερινών δραστηριοτήτων.

Το αθλητικό rafting συνίσταται στην κατάβαση του ποταμού με συγκεκριμένη διαδρομή, μέσω επιλεγμένων εμποδίων, στον μικρότερο χρόνο. Κάθε φουσκωτή βάρκα κατεβαίνει τη διαδρομή περνώντας υποχρεωτικά από τα επιλεγμένα εμπόδια (έγκυρη κατάβαση) και, με βάση το χρόνο της, οι πίνακες τερματισμού δίνουν τη θέση της στη γενική κατάταξη. H πρώτη βάρκα για παράδειγμα θα έχει αναγκαστικά θέση $$1$$. Η δεύτερη $$1$$ ή $$2$$ και η $$N$$-οστή οποιαδήποτε θέση από $$1$$ έως $$N$$.

## Πρόβλημα

Nα αναπτύξετε ένα πρόγραμμα σε μια από τις γλώσσες του IOI (PASCAL, C, C++, Java) το οποίο αφού διαβάσει τη θέση που παίρνει η κάθε σχεδία στη γενική κατάταξη μέχρι εκείνη τη στιγμή, θα υπολογίζει την τελική θέση κάθε σχεδίας μετά το τέλος του αγώνα.

## Αρχεία εισόδου

Τα αρχεία εισόδου με όνομα **rafting.in** είναι αρχεία κειμένου με την εξής δομή: Η πρώτη γραμμή έχει έναν ακέραιο αριθμό $$N$$, το πλήθος των σχεδιών που λαμβάνουν μέρος στον αγώνα. Η δεύτερη γραμμή περιέχει $$N$$ ακέραιους αριθμούς χωρισμένους ανά δύο με ένα κενό διάστημα: τις θέσεις στη γενική κατάταξη που έχει μέχρι εκείνη τη στιγμή η αντίστοιχη σχεδία.

## Αρχεία εξόδου

Τα αρχεία εξόδου με όνομα **rafting.out** είναι αρχεία κειμένου με την εξής δομή: Έχουν μία γραμμή που περιέχει $$N$$ ακέραιους αριθμούς, όσες και οι σχεδίες, χωρισμένους ανά δύο με ένα κενό διάστημα. Κάθε αριθμός πρέπει να είναι ο αύξων αριθμός της σχεδίας που θα καταλάβει την αντίστοιχη θέση στην τελική κατάταξη.

## Παραδείγματα Αρχείων Εισόδου - Εξόδου

**1<sup>o</sup>**

| **rafting.in**      | **rafting.out** |
| :--- | :--- |
| 10 <br> 1 2 3 4 5 6 7 8 9 10 | 1 2 3 4 5 6 7 8 9 10 |

**2<sup>o</sup>**

| **rafting.in**      | **rafting.out** |
| :--- | :--- |
| 10 <br> 1 1 1 1 1 1 1 1 1 1 | 10 9 8 7 6 5 4 3 2 1 |

**3<sup>o</sup>**

| **rafting.in**      | **rafting.out** |
| :--- | :--- |
| 7 <br> 1 1 3 2 3 1 5 | 6 2 4 5 7 1 3 |

*Εξήγηση:* Στο 1<sup>ο</sup> παράδειγμα, κάθε σχεδία που τερματίζει κάνει χειρότερο χρόνο από τις προηγούμενες και κατατάσσεται τελευταία, ενώ στο 2<sup>ο</sup> κάθε σχεδία κάνει καλύτερο χρόνο από τις προηγούμενες και κατατάσσεται πρώτη.

## Περιορισμοί:

 * Για περιπτώσεις ελέγχου συνολικής αξίας 50%, θα είναι:
   $$1 \leq N \leq 10.000$$
 * Για περιπτώσεις ελέγχου συνολικής αξίας 100%, θα είναι:
   $$1 \leq N \leq 500.000$$

**Προσοχή!** Φροντίστε να διαβάζετε την είσοδο και να εκτυπώνετε την έξοδο αποδοτικά, ειδικά αν προγραμματίζετε σε C++ ή Java.

 * **Μορφοποίηση:** Στην είσοδο αλλά και στην έξοδο, κάθε γραμμή τερματίζει με έναν χαρακτήρα newline.
 * **Μέγιστος χρόνος εκτέλεσης:** $$1$$ sec.
 * **Μέγιστη διαθέσιμη μνήμη:** $$64$$ MB.