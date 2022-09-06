---
layout: class
title: How to install Apache Tomcat on Linux
slug: installing-tomcat-on-linux
categories: first-year first-semester
img-path: ../assets/img/blogs/installing-tomcat-on-linux
---

# {{page.title}}

Οι εφαρμογές της Java μπορούν να τρέξουν μέσο του Apache Tomcat, έναν web server ανοικτού κώδικα. Είναι ο πιο ευρέως χρησιμοποιούμενος web server για web applications σε Java. Χρησιμοποιείται από εκατοντάδες επιχειρήσεις, συμπεριλαμβανομένων των MIT, Alibaba και eBay.

Αυτό το άρθρο θα σας καθοδηγήσει στη διαδικασία εγκατάστασης του **Tomcat 8.5.82**. Τα παραδείγματα κώδικα που παρέχω έχουν δοκιμαστεί στο **MX Linux (Debian)** αλλά η γενική διαδικασία είναι ίδια για όλα τα distributions (distros). Αυτό σημαίνει ότι ανεξάρτητα από ποιο distro έχετε απλά ακολουθήστε το άρθρο και όπου υπάρχει κάποιο command που λειτουργεί αποκλειστικά σε distos βασισμένα στο Debian θα σας έχω εναλλακτικές.

## Apache Tomcat requirements

Γενικά εκτός αν κάποιος θέλει να κάνει compile τον Tomcat μόνος του, έχουμε μόνο ένα requirement.

Και αυτό είναι η **Java**. Εδώ είναι και η μόνη διαφορά σε ολόκληρη την διαδικασία όπου το distro που έχετε παίζει ρόλο. Θα πρέπει να εγκαταστήσουμε το **JDK** για να μπορέσουμε να χρησιμοποιήσουμε τον Tomcat.

Πριν όμως πάμε να κάνουμε την εγκατάσταση της Java, βεβαιωθείτε ότι δεν την έχετε ήδη εγκαταστήσει. Για να δούμε αν έχουμε εγκατεστημένη κάποια έκδοση της Java απλά τρέχουμε την εξής εντολή:

```sh
java --version
```

![Image: Terminal showing the installed java version]({{page.img-path}}/java-version.png)

Αν μας βγάλει κάποιο αποτέλεσμα πάμε στο επόμενο βήμα αλλίως συνεχίζουμε εδώ.

Στην περίπτωση που δεν έχουμε κάποια έκδοση της Java εγκατεστημένη μπορούμε πολύ εύκολα να την κατεβάσουμε. Για ευκολία θα χρησιμοποιήσουμε τον _package manager_ που έρχετε με το distro μας για να κατεβάσουμε μία έκδοση της Java.

* **Debian** based distributions

  ```bash
  sudo apt install default-jdk
  ```

* **Fedora**

  Μπορείτε να κατεβάσετε οποιαδήποτε έκδοση της Java, απλά εγώ θα αφήσω εδώ το πακέτο με την τελευταία έκδοση της.
  ```bash
  sudo dnf install java-latest-openjdk 
  ```

* **Arch**
  
  Για την τελευταία έκδοση της Java.
  ```bash
  sudo pacman -S jre-openjdk jdk-openjdk
  ```

## Installing and Setting up Apache Tomcat

Η διαδικασία είναι απλή και πλέον είναι ίδια για κάθε distro που μπορεί να τρέχετε.

### Step 1 - Go to their Website

Πάμε στο [website](https://tomcat.apache.org/download-80.cgi&#8.5.82) τους να κατεβάσουμε το tar αρχείο κάτω από την κατηγορία Core.

  ![]({{page.img}}/tomcat-site.png)

### Step 2 - Download the zipped tomcat binary

Αποθηκεύουμε το αρχείο με όνομα **apache-tomcat-8.5.82.tar.gz** σε έναν φάκελο της επιλογής μας.

  ![]({{page.img-path}}/downloaded-tomcat.png)

  Να σημειωθεί ότι εγώ το έχω σωσει στον φάκελο **Downloads**, το οποίο δεν είναι και η καλύτερη τοποθεσία αλλά απλά θέλω να δείξω την διαδικασία.

### Step 3 - Unzip it

![]({{page.img-path}}/unzip.png)

### Step 4 - Locate the .bashrc file

Το αρχείο **.bashrc** είναι ένα συγκεκριμένο αρχείο για το shell enviroment μας και βρίσκεται στο `~/.bashrc`. Αν δεν υπάρχει πρέπει απλός να το δημιουργήσουμε με το εξής command:

  ```bash
  cd ~ && touch .bashrc
  ```

**Σημείωση**: Αν χρησιμοποιήτε κάποιο άλλο shell (πχ **zsh**) τότε πρέπει να κάνετε την ίδια διαδικασία για το αντίστοιχο αρχείο. Για το zsh για παράδειγμα θα πρέπει να βρείτε το αρχείο **.zshrc** όπου και αυτό θα βρίσκεται εδώ `~/.zshrc`.

![]({{page.img-path}}/locate-bashrc.png)

### Step 5 - Add a new variable

Για την σωστή λειτουργία του Tomcat πρέπει να ορίσουμε ένα νέο _Enviroment variable_ στο **.bashrc** αρχείο. Η νέα αυτή μεταβλητή θα περιέχει το **path** στον unzipped φάκελο.

![]({{page.img-path}}/copy-path.png)

Τώρα που κάναμε copy το path, στην περίπτωση μου είναι `/home/vm/Downloads/apache-tomcat-8.5.82`, πρέπει να ανοίξουμε το `.bashrc` αρχείο με οποιοδήποτε editor της επιλογής μας.

![]({{page.img-path}}/new-variable.png)

Αφότου το ανοίξουμε πάμε σε μία κενή γραμμή και γράφουμε το εξής:

```bash
export CATALINA_HOME="/home/vm/Downloads/apache-tomcat-8.5.82"
```

Προφανώς το δικό σας path θα διαφέρει. Κάνουμε **save** και κλείνουμε το terminal.

### Step 6 - Starting Apache Tomcat

Τώρα είμαστε έτοιμοι να τρέξουμε τον Tomcat. Για να το κάνουμε αυτό πάμε στον φάκελο όπου τον κάναμε unzip και μετά πάμε στον φάκελο **bin**. Το μόνο που μένει είναι να τρέξουμε το script που παρέχουν με όνομα `startup.sh` και ο Tomcat θα αρχίσει.

```bash
sudo ./startup.sh
```

![]({{page.img-path}}/startup.png)

Αν πήγαν όλα καλά θα πρέπει να δούμε το μήνυμα **Tomcat started**. Σε κάθε άλλη περίπτωση επανεξετάζουμε τα παραπάνω βήματα.

### Step 7 - Visiting localhost:8080

By default ο Tomcat τρέχει στο port 8080 οπότε για να βεβαιωθούμε ότι όντως τρέχει απλά πάμε στον browser της επιλογής μας με το link [http://localhost:8080/](http://localhost:8080/).

![]({{page.img-path}}/localhost.png)


## Conclusion

Κάναμε εγκατάσταση τον **Apache Tomcat 8.5.82** για οποιοδήποτε Linux distribution, η εγκατάσταση είναι απλή και γρήγορη και γενικά δεν θα αντιμετωπίσετε κάποιο error αν ακολουθήσετε όλα τα βήματα με την σειρά. Τώρα που ολοκληρώσατε την εγκατάστασή σας, μπορείτε να αναπτύξετε εφαρμογές σε Java και να αρχίσετε να πειραματίζεστε με JSPs (Java Server Pages), servlets και άλλες τεχνολογίες.