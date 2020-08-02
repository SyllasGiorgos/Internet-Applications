# Internet-Applications
Θα χρησιμοποιήσω το api free nba (https://rapidapi.com/theapiguy/api/free-nba) ή άλλα datasets σχετικά με το nba από το σύνδεσμο που στειλατε, θα κάνω κάποια calls στο api αυτό για να γεμίσω μια βάση μου τοπική (my SQL λογικά) με πληροφορίες όπως παίκτες και ομάδες και μετά θα φτιάξω ένα back end σε java, δεν ξέρω ακόμα ποιο framework, που θα επικοινωνεί με ένα front end σε js,css,html.θα υλοποιούνται λειτουργίες του στυλ: με input το όνομα ενός παίκτη φέρε μου στοιχεία για αυτόν . Για μια χρονιά που θα ορίσει ο χρήστης φέρε μου τους δέκα καλύτερους σκορερ και άλλα παρομοια. 
#Περιεχόμενα

Nba-backend-> Το gradle java project μου που υλοποιεί το back-end/////
Nba-frontend-> Το react js project για το front-end///////
SqlDump-> Τα dump που θα κάνει κάποιος import για να στήσει την αντίστοιχη mysql βάση στον υπολογιστή του


Οδηγίες Εγκατάστασης-> Οδηγίες για το πως θα εγκαταστήσει κάποιος τα προγράμματα αυτά στον υπολογιστή του
Οδηγίες εγκατάστασης Project στο μάθημα Διαδίκτυο και Εφαρμογές

Versions που χρησιμοποίησα σε Windows 10 και σίγουρα δουλεύουν(πολύ πιθανό και πολλές άλλες)

Για το back-end:

-java 11 (Το gradle αντιμετωπίζει προβλήματα με την java 14. Επομένως χρησιμοποίησα την java 11, συγκεκριμένα την έκδοση 11.0.6)
-gradle 6.5.1 (Λογικά δεν θα έχει θέματα και με παλιότερες εκδόσεις)

Για την βάση:

-mysql 8.0.19 Χρησιμοποίησα το mysql community server και το workbench

Για το front-end:

-node v12.6.1 και yarn 1.22.0

Για την εγκατάσταση και εκτέλεση του project:

Καταρχήν κάνουμε git clone το repository. Φτιάχνουμε μία βάση με το όνομα nba. Κάνουμε στη βάση αυτήν import τα dump που βρίσκονται στο φάκελο SqlDump. Κατευθυνόμαστε στο φάκελο /Nba-backend/src/main/resources/   και δημιουργούμε, ακολουθώντας τις οδηγίες από το app-default.properties ένα αρχείο app.properties με τα στοιχεία που χρειάζονται για τη σύνδεσή μας στη βάση.

Ανοίγουμε μετά ένα command line και εκτελούμε: 
cd /Nba-backend/ 
Εκεί εκτελούμε gradle appRun (θα πάρει λίγη ώρα την πρώτη φορά)

Επίσης μόλις σηκωθεί ο server ανοίγουμε ένα παράθυρο browses, πλοηγούμαστε στο https://localhost:8765/nba/api/AllPlayers/James Harden
και εκεί πατάμε advanced options και μετά accept the risk and continue. Αυτό συμβαίνει διότι δεν έχουμε authorized ssl certificate.

Σε ένα άλλο command line:
cd /Nba-frontend/
Εκεί εκτελούμε yarn install και όταν τελείωσει yarn start

Η εφαρμογή μας είναι έτοιμη :)
