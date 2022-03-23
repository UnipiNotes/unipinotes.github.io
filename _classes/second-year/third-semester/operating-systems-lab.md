---
layout: class
title: Λειτουργικά Συστήματα | Lab Notes
slug: operating-systems-lab
categories: second-year third-semester
---

# Λειτουργικά Συστήματα [C/Bash]

## Lab Notes

<br />

## Installing a VM

Δύο είναι οι πολύ καλές επιλογές για τα VM:

* **VM Ware** 
* **Virtual Box**

### Windows

* [How to Install VMware Workstation Player in Windows 10](https://server.vpnwp.com/workstation/how-to-install-vmware-workstation-player-in-windows-10/)

* [How to Install VirtualBox on Windows 10 Step by Step Tutorial for Beginners](https://www.cyberpratibha.com/install-virtualbox-on-windows-10/)

<br />

### MacOS

* [How to Install a Windows 10 VirtualBox VM on macOS](https://www.howtogeek.com/657464/how-to-install-a-windows-10-virtualbox-vm-on-macos/)

<br />

## Choosing a Linux Distribution

Δεν υπάρχει σωστή ή λάθος επιλογή, απλά ψάχνετε και διαλέγεται ότι σας αρέσει. Εγώ θα αφήσω εδώ μία πολύ μικρή λίστα με μία σύντομη περιγραφή για το κάθε ένα αλλά από εκεί και πέρα ψάξτε μόνοι σας.


* **[Ubuntu](https://ubuntu.com/)**
    
	Το χρησιμοποιεί και ο Κοντζανικολάου και είναι από τα πιο γνωστά στον κόσμο. Είναι βασιμσένο στο **Debian** το οποίο το κάνει πολύ σταθερό και συμβατό με πάρα πολλά πράγματα.

	<img src="https://www.dropbox.com/s/vtai15f9i3sf66r/ubuntu.png?raw=1" alt="ubuntu.png" width="75%"/>



* **[Linux Mint](https://linuxmint.com/)**

	Επίσης από τα πιο γνωστά στον κόσμο και το κάνουν promote σε beginners που δοκιμάζουν Linux για πρώτη φορά. Αυτό γιατί το UI του θυμιζει πολύ τα Windows αλλά και επειδή είναι εύκολο στην χρήση. Τέλος και αυτό είναι βασισμένο στο **Ubuntu**.

	<img src="https://www.dropbox.com/s/r1wk0pgmkc3llwd/linux_mint.png?raw=1" alt="linux_mint.png" width="75%"/>

* **[MX Linux](https://mxlinux.org/)**
	
	To MX Linux είναι βασισμένο στο **Debian** και είναι γνωστό για το πόσο ελαφρύ είναι. Επίσης είναι πολύ καλό για beginners καθώς οι developers παρέχουν δικά τους εργαλεία για διάφορες καθημερινές ανάγκες.
	
	<img src="https://www.dropbox.com/s/mxrn2vt5wj7ae5e/mx_linux.jpg?raw=1" alt="mx_linux.jpg" width="75%"/>

* **[PopOS](https://pop.system76.com/)**

    Επίσης βασισμένο στο **Ubuntu** είναι πολύ γνωστό και σταθερό. Μία από τις καλύτερες επιλογές, ειδικά με την καινούρια τους έκδοση.
	
	<img src="https://www.dropbox.com/s/qvga3zgc6oa0z6c/pop_os.jpeg?raw=1" alt="pop_os.jpeg" width="75%"/>

* **[ZorinOS](https://zorinos.com/)**
	
	Έχει ωραία εμφάνιση και είναι λειτυργικό. Είναι βασισμένο στο **Ubuntu** οπότε και πάλι το εργαστήριο     θα γίνεται με άνεση. Είναι επίσης γνωστό για όσους δοκιμάζουν για πρώτη φορά Linux.

	<img src="https://www.dropbox.com/s/s1p2wwjwgcecb4b/zorin_os.png?raw=1" alt="zorin_os.png" width="75%"/>

* **[elementaryOS](https://elementary.io/)**
    
	Γνωστό για την εμφάνιση του καθώς έρχεται preconfigured να μοιάζει ως macOS. Είναι βασισμένο στο **Ubuntu** οπότε πολύ εύκολα γίνεται η δουλειά του εργαστηρίου και από αυτό.

	<img src="https://www.dropbox.com/s/0d08ykw1z3yliym/elementary_os.jpeg?raw=1" alt="elementary_os.jpeg" width="75%"/>


* **[Manjaro](https://manjaro.org/)**

	Σε αντίθεση με τα προηγούμενα είναι βασισμένο στο **Arch**. Είναι αυτό που χρησιμοποιώ εγώ και γενικά έχει αρκετές διαφορές με όλα τα προηγούμενα.

	<img src="https://www.dropbox.com/s/ucifswsx8vmangx/manjaro_xfce.png?raw=1" alt="manjaro_xfce.png" width="75%"/>

* **[Tumbleweed](https://www.opensuse.org/#Tumbleweed)**

	<img src="https://www.dropbox.com/s/s9b72ajgest5137/tumbleweed.jpg?raw=1" alt="tumbleweed.jpg" width="75%"/>

<br />

## Installing a Linux Distribution inVBOX

[How to Install Ubuntu on VirtualBox: Detailed Overview](https://www.nakivo.com/blog/install-ubuntu-on-virtualbox-virtual-machine/)

**Σημείωση**: Η διαδικασία είναι ίδια και για όλα τα άλλα distributions που έχω αναφέρει. 

<br />

## Bash and Terminal Commands

<br />

### Commands

**Σημείωση**: Θα αναφέρω Commands τα οποία είναι κυρίως χρήσιμα για το μάθημα αλλά κιαι κάποια γενικής χρήσης. Παρόλα αυτά θα εστιάσω σε commands που αφορούν το εργαστήριο. Επίσης όπου έχω ` `` ` βάζετε εσείς ότι θέλετε. 

<br />

```bash
ls
```
Δείχνει όλα τα αρχεία που περιλαμβάνει ο φάκελος που βρισκόμαστε (χωρίς τα hidden αρχεια).

<br />

```bash
ls -l
```
Το ίδιο με το απλό `ls` απλά τώρα έχουμε κάποιες extra πληροφορίες για το κάθε αρχείο.

<br />

```bash
touch `new_file`
```
Δημιουργεί ένα καινούριο αρχείο με το όνομα που του παρέχουμε (αν αυτο δεν υπάρχει).

<br />

```bash
cat `file`
```
Εκτυπώνει το περιεχόμενο ενός αρχείο. Αν για παράδειγμα έχουμε ένα αρχείο `test.txt` στο οποίο είχαμε γράψει `Hello, World!` τότε η εντολή `cat test.txt` θα εκτύπωνε `Hello, World!`.

<br />

```bash
mv `file` `destination`
```
Μετακινεί ένα αρχείο στον φάκελο της αρεσκείας μας. Είναι χρήσιμο αν θέλουμε να κάνουμε **rename** ένα αρχείο.

Αν για παράδειγμα έχουμε ένα αρχείο με όνομα `test.txt` μπορούμε να το μετονομάσουμε γράφοντας `mv test.txt renamed.txt`.

<br />


```bash
cp `file` `destination`
```
Κάνει **copy** ένα αρχείο στο destination που παρέχουμε.


<br />

```bash
rm `file`
```
Διαγράφει ένα αρχείο.


<br />

```bash
wc `file`
```
Εκτυπώνει τον αριθμό των χαρακτήρων, λέξεων και γραμμών που περιέχει ένα αρχείο.

```bash
wc -w `file`
```
Εκτυπώνει τον αριθμό των λέξεων μόνο .

```bash
wc -c `file`
```
Εκτυπώνει τον αριθμό των χαρακτήρων μόνο.

<br />

```bash
sort `file`
```
Ταξινομεί τα περιεχόμενα ενός αρχείο γραμμή γραμμή με αλφαβιτική σειρά (α -> ω).

<br />

```bash
sort -r `file`
```
Ταξινομεί τα περιεχόμενα ενός αρχείο γραμμή γραμμή προς την ατνίθετη κατεύθηνση (ω -> α).

<br />

```bash
mkdir `new_directory`
```

Δημιουργεί έναν νέο φάκελο.

<br />

```bash
rmdir `directory`
``` 
Διαγράφει έναν *άδειο* φάκελο.

<br />

```bash
rmdir -rf `directory`
```
Διαγράφει έναν φάκελο ακόμα και ας έχει περιεχόμενα.

<br />

```bash
cd `directory`
```
Μετακινούμαστε σε άλλον φάκελο.

<br />

```bash
cd ..
```
Μετακινούμαστε στον parent φάκελο. Δηλαδή αν έχουμε ένα φάκελο `Documents/Work` και βρισκόμαστε στον φάκελο `Work` αν κάνουμε `cd ..` θα πάμε στον φάκελο `Documents`.

<br />

```bash
chmod -options `file
```
Ένα πολύ βασικό command καθώς θα το χρειαστούμε και αργότερα για τα bash αρχεία μας. Μας επιτρέπει να αλλάξουμε τα `read`, `write` και `execute` permissions ενός αρχείου.


Κάθε αρχείο έχει ορισμένα δικαιώματα. Αν για παράδειγμα δημιουργήσουμε ένα νέο bash αρχείο `touch test.sh` και εκτελέσουμε την εντολή `ls -l` θα δούμε τέρμα αριστερά κάτι παρόμοιο σε αυτό `-rw-rw-r--`.

Στην ουσία είναι τα permissions του αρχείου, `r` = read, `w` = write και `x` = execute.

Βλέπουμε όμως ότι η άδεια να διαβάσουμε αυτό το αρχείο `r` επαναλαμβάνεται 3 φορές. Αυτό γίνεται γιατί υπάρχουν 3 διαφορετικοί users.

Συγκεκριμένα το λεγόμενο `ugo`, `u` = user, `g` = group και `o` = other.

<br />

Ο κάθε χρήστης μπορεί να έχει ίδια αλλά και διαφορετικά permissions. Σημασία έχει πως τα permissions που δίνουμε σε κάθε χρήστη ακολουθούν αυστηρά την σειρά `ugo`.

Δηλαδή μπορούμε να δούμε ότι το αρχείο `test.sh` έχει `r` και `w` permissions για τον `user`, `r` και `w` permissions για τον `group` και `r` permission για τον `other`.

Μπορούμε εύκολα να δώσουμε permissions στον κάθε χρήστη ξεχωριστά αλλά και μαζικά. Ας δώσουμε σε όλους τους χρήστες το δικαίωμα να κάνουν execute `x` το αρχείο.

```bash
chmod +x test.sh
ls -l
```
Βλέπουμε ότι τώρα τα permissions είναι τα εξής: `-rwxrwxr-x`. Το ίδιο μπορούμε να κάνουμε άμα θέλουμε να αφαιρέσουμε ομαδικά ένα permission.

```bash
chmod -x test.sh
ls -l
```
Τώρα τα permissions είναι όπως όταν δημιουργήσαμε το αρχείο.

Αν δεν θέλουμε να κάνουμε μαζική αλλαγή τότε απλώς βάζουμε τον χρήστη που θέλουμε να επιρεάσουμε.

```bash
chmod u=rwx test.sh
ls -l
```

Τώρα έχουμε αυτά τα permissions: `-rwxrw-r--`.

**Σημείωση**: Σε αυτές τις περιπτώσεις πρέπει να αναφέρουμε όλα τα permissions αλλιώς δεν θα γίνει αυτό που περιμένουμε. Δηλαδή αν γράφαμε `chmod u=x test.sh` τότε θα βγάζαμε όλα τα permissions που είχε και απλά θα βάζαμε το execute permission `x`.

Τέλος μπορούμε να αλλάξουμε τα permissions με αριθμούς. Κάθε permission έχει μία αριθμιτηκή τιμή: `r` = 4, `w` = 2 και `x` = 1.

Οπότε αν έχουμε `-rwx---r--` τότε με αριθμούς θα το γράφαμε: 
```txt
u = r + w + x = 4 + 2 + 1 = 7

g = 0

o = r = 4
```

Άρα αν θέλαμε να δώσουμε τα δικαιώματα `-rwxrw-r--` στο αρχείο μας θα γράφαμε:

```bash
chmod 764 test.sh
ls -l
```
Πλέον το αρχελιο μας έχει τα εξής δικαιώματα: `-rwxrw-r--`.

<br />

```bash
grep `string` `file`
```
Ψάχνει να βρει μέσα σε ένα αρχείο το `string` που του παρέχουμε. Εκτυπώνει ολήκληρες τις προτάσεις που βρήκε το `string`.

<br />

```bash
grep -o `string` `file`
```
Ψάχνει να βρει μέσα σε ένα αρχείο το `string` που του παρέχουμε. Εκτυπώνει μόνο το `string` αν το βρει.

<br />

```bash
grep -i `string` `file`
```
Ψάχνει να βρει μέσα σε ένα αρχείο το `string` που του παρέχουμε αλλά χωρίς να είναι case sensitive.

<br />

```bash
grep -o `string` `file` > `file`
```
Μπορούμε να αποθηκεύσουμε το αποτέλεσμα από οποιοδήποτε command σε κάποιο αρχείο χρησιμοποιόντας το `>`. 

Άρα για παράδειγμα αν έχουμε ένα αρχείο `test.txt` και μέσα έχουμε `Hello, World!` και τρέξουμε το command `grep -o 'Hello' test.txt > result.txt` το πρώτο command θα βρει ότι έχουμε γράψει `Hello` μέσα στο αρχείο και στην συνέχεια αντί να το εκτυπώσει, το μεταφέρει και το γράφει στο αρχείο `result.txt`.

**Σημείωση**: Αν το αρχείο `result.txt` δεν υπάρχει τότε το δημιουργεί αυτόματα.

<br />

```bash
cat `file` >> `another_file` 
```

Ο χαρακτήρας `>>` μας δίνει την δυνατότητα να κάνουμε **append** σε ένα αρχείο. Στο από πάνω παράδειγμα κάνω `cat file` δηλαδή *εκτύπωση στο terminal τα περιεχόμενα του αρχείου* αλλά αντί να τα εκτυπώσω απλά τα προσθέτω στο τέλος ενός άλλου αρχείου `another_file`.

<br />

Ένα από τα πιο σημαντικά commands είναι το `|`. Το πως λειτουργεί είναι πολύ απλό, στην ουσία παίρνει το αποτέλεσμα από ένα command και το παρέχει ως είσοδο σε ένα άλλο command.

```bash
ls -l | sort -r
```

Εδώ το αποτέλεσμα από το command `ls -l` θα περάσει στο επόμενο command το `sort`.  Στην ουσία θα εκτυπώσει τα αρχεία και τις πληροφορίες τους ταξινομημένα.

Άλλο παράδειγμα:

```bash
grep -io "hello" test.txt | wc -w 
```

Εδώ βρίσκουμε όλες τις λέξεις `hello` που υπάρχουν στο αρχείο `test.txt` (είτε είναι γραμμένες με κεφαλαία είτε όχι) και απλά μετράμε πόσες βρήκαμε με το command `wc -w`.

<br />

## Εφαρμογή Εντολών

1. Είμαστε στο **Home** directory και χωρίς να μετακινηθούμε από αυτόν πρέπει να δημιουργήσουμε δύο *φακέλους* (test, other) καθώς και τα *αρχεία* (012, 021, 120, 102, 201, 210).

**Λύση**

```bash
mkdir test other && touch test/{012,021,120,102,201,210}.txt
```

<br>

<details style="cursor: pointer">
	 <summary>Screenshots Here</summary>
	 <br>
	1. Το Home πριν να τρέξουμε το command.
	 <img src="https://www.dropbox.com/s/onrazpenqdisij3/before_command.png?raw=1" alt="home directory before running the command above" width="100%"/>

    2. Το Home directory μας αφότου τρέξουμε το command.
   <img src="https://www.dropbox.com/s/aq437j9xg03x5ua/home_after_command.png?raw=1" alt="home directory after running the command above " width="100%"/>

	3. Ο φάκελος test που περιέχει όλα τα αρχεία txt που θέλουμε.
   <img src="https://www.dropbox.com/s/b1o5jwq8f1lzymu/new_folder_after_command.png?raw=1" alt="the newly created folder and what it contains" width="100%"/>

</details>


<br />

 2. Χωρίς να μετακινηθούμε από το **Home** directory και με μία μόνο εντολή να αντιγράψουμε τα *αρχεία* (xyz, xzy, yxz) στον *φάκελο* (other). Επίσης πρέπει να παρέχετε μόνο *δύο ορίσματα* και δεν επιτρέπεται η χρήση των χαρακτήρων `{` και `}`. Για να βρείτε τους χαρακτήρες (x, y, z) πρέπει να κάνετε τις εξής πράξεις (x = E mod 3), (y = (E+1) mod 3) και (z = (E+2) mod 3), όπου **Ε** το τελευταίο ψηφίο του **ΑΜ** σας.
	<br />
	**Λύση**
	
	Έστω ότι Ε = 5
	<br />
	x = 5 mod 3 = 2
	y = 6 mod 3 = 0
	z = 7 mod 3 = 1
	<br />
	Άρα πρέπει να αντιγράψουμε μόνο τα αρχεία: **201**, **210** και **021**
	```bash
	cp test/[02]?[01].txt other/
	```
	
	<br />
	
	**Επεξήγηση**
	
	Πρέπει να αντιγράψουμε τα αρχεία 201, 210 και 021. Παρατηρούμε ότι όλα τα αρχεία ξεκινάνε είτε με το ψηφίο *2* είτε με το ψηφίο *0*. Γι αυτό λέμε *[02]* δηλαδή περιλαμβάνουμε ότι αρχίζει είτε με *2* είτε με *0*. Μετά έχουμε βάλει τον χαρακτήρα *?* το οποίο σημαίνει ότι εκεί μπορεί να υπάρχει οποιοσδήποτε χαρακτήρας. Όντως αμα παρατηρήσουμε τα αρχεία που πρέπει να αντιγράψουμε, σαν δεύτερο ψηφίο υπάρχουν όλοι οι πιθανοί αριθμοί (0, 1, 2) άρα δεν μας νοιάζει να έχουμε κάποιο συγκεκριμένο ψηφίο σε αυτή την θέση. Τέλος βάλαμε *[0-1]* (θα μπορούσαμε να βάλουμε και [01] γιατί προφανώς δεν έχει διαφορά) και αυτό γιατί πολύ απλά το τελικό ψηφίο και στα τρία αρχεία είτε είναι *0* είτε είναι *1*.
	<br />
	<details style="cursor: pointer">
		 <summary>Screenshots Here</summary>
		 <br>
		1. Το other directory πριν να τρέξουμε το command.
		 <img src="https://www.dropbox.com/s/pjx5447w7yn9vm4/before_cp.png?raw=1" alt="other directory before executing the above command" width="100%"/>

		2. Το command που πρέπει να τρέξουμε.
	   <img src="https://www.dropbox.com/s/nhfquhzl43it3q3/cp_command.png?raw=1" alt="executing the above command " width="100%"/>

		3.Ο φάκελος other που περιέχει όλα τα αρχεία txt που έπρεπε να αντιγράψουμε.
	   <img src="https://www.dropbox.com/s/8fbf7jgknag7d6o/after_cp.png?raw=1" alt="other directory after executing the above command" width="100%"/>

	</details>
	
<br />


 3. Υπολογίστε τα xyz κάνοντας τις εξείς πράξεις (x = Γ mod 8), (y = Δ mod 8) και (z = Ε mod 8), όπου Γ Δ Ε τα τρία τελευταία ψηφία του ΑΜ σας. Στην συνέχεια χωρίς να μετακινηθήτε από το **Home** directory εκτελέστε την εντολή `chmod xyz ~/test/012.txt` (χωρίς όμως να χρησιμοποιήσετε αριθμητικές τιμές).
	
	<br />
	
	**Λύση**
	
	Έστω ότι Γ = 1, Δ = 9, Ε = 5.
	
	<br />
	
	x = 1 mod 8 = 1
	y = 9 mod 8 = 1
	z = 5 mod 8 = 5
	
	<br />
	
	Άρα πρέπει να αλλάξουμε τα δικαιώματα του αρχείου *012* στις **115**.
	
	```bash
	chmod u=x,g=x,o=rx test/012.txt
	```
	
	<br />
	
	**Επεξήγηση**
	
	Εφόσον δεν πρέπει να χρησιμοποιήσουμε τις αριθμητικές τιμές για να αλλάξουμε τα δικαιώματα του αρχείου *012* πρέπει να χρησιμοποιήσουμε τους χαρακτήρες `r w x`. Γνωρίζουμε ότι `r = 4`, `w = 2` και `x = 1`. Οπότε το μόνο που μένει είναι να βρούμε τον σωστό συνδυασμό χαρακτήρων ώστε να φτιάξουμε τα δικαιώματα του αρχείου.
	Εφόσον πρέπει να έχουμε `115` σημαίνει ότι έχουμε `u=1,g=1,o=5` άρα με χαρακτήρες έχουμε: `u=x,g=x,o=rx`. Το `u` και το `g` νομίζω είναι πολύ απλά να τα καταλάβουμε, το `o` όμως είναι συνδυασμός του `r` και του `x` αυτό γιατί `r = 4`  και `x = 1` οπότε για να φτιάξουμε το `5` χρησιμοποιούμε και τα δύο. 
	
	<br />
	<details style="cursor: pointer">
		 <summary>Screenshots Here</summary>
		 <br>
		1. Τα δικαιώματα του αρχείου 012.txt πριν να τρέξουμε το command.
		 <img src="https://www.dropbox.com/s/g1m1a2k1hyier37/before_chmod.png?raw=1" alt="permissions of 012.txt before executing the above command" width="100%"/>

		2. Το command που πρέπει να τρέξουμε.
	   <img src="https://www.dropbox.com/s/aosl43op9qr33x4/chmod_command.png?raw=1" alt="executing the above command " width="100%"/>

		3. Τα δικαιώματα του αρχείου 012.txt μετά την εκτέλεση του command (και εμφάνιση του με αριθμούς αν σας μπερδεύουν οι χαρακτήρες).
	   <img src="https://www.dropbox.com/s/rlhzs922q5wgp2d/after_chmod_chars.png?raw=1" alt="permissions of 012.txt after executing the above command" width="100%"/>
		<br>
	 	<img src="https://www.dropbox.com/s/3rdbfw5f9mm5vfy/after_chmod_nums.png?raw=1" alt="permissions of 012.txt after executing the above command in numbers" width="100%"/>
	</details>
	
	<br />