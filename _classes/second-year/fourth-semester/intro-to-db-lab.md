---
layout: class
title: Βάσεις Δεδομένων | Theory Notes
slug: intro-to-db-lab
categories: second-year fourth-semester
sf: second-year/fourth-semester
---

# Βάσεις Δεδομένων [SQL]

## Lab Notes

<br />

[Theory Notes](/notes/{{page.sf}}/intro-to-db-theory)

<br />

## Installing PostgeSQL

<br />

### Windows

 1. [Download PostgreSQL for Windows](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads)
 2. [Download pgAdmin4 for Windows](https://www.pgadmin.org/download/pgadmin-4-windows/)

<br />

### MacOS

1. Κάνουμε download την PostgreSQL (διαλέγουμε έναν από τους δύο τρόπους):
	*  Installing using Homebrew:
	   
	  ```
	   brew install postgresql
	 ```
	* Using the installer:
	    
		[Download PostgreSQL for macOS](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads)
	
2. [Download pgAdmin for macOS](https://www.pgadmin.org/download/pgadmin-4-macos/)


<br />

### Linux

* Debian
    
1. Install PostgreSQL using apt:

	```bash
	sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
	wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
	sudo apt-get update
	sudo apt-get install postgresql-XX
	```
	**Σημείωση**: Στο τελευταίο command όπου XX βάζουμε όποια έκδοση της PostgreSQL θέλουμε να κατεβάσουμε.

2. Download pgAdmin4 for Debian based distros using apt:
  ```bash
	sudo curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add
	sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'
	sudo apt-get install pgadmin4
	```


* Arch

1. Install PostgreSQL using pacman:

	```bash
	sudo pacman -S postgresql
	```

2. [Download pgAdmin for Arch based distros](https://archlinux.org/packages/community/x86_64/pgadmin4/)
	
	**Σημείωση**: Θα το εγκαταστήσετε μέσω του AUR οπότε πάντα να τσεκάρετε το πακέτο.


<br />

## Choosing an IDE or a Text Editor

Ως επιλογές έχουμε τις εξής:

### Text Editors
1. [Visual Studio Code](https://code.visualstudio.com/#alt-downloads) [Windows/MacOS/Linux]
2. [Sublime](https://www.sublimetext.com/download) [Windows/MacOS/Linux]
3. [Atom](https://atom.io/) [Windows/MacOS/Linux]
4. [Emacs](https://www.gnu.org/software/emacs/) [Windows/MacOS/Linux]
5. [Notepad++](https://notepad-plus-plus.org/) [Windows]


**Σημείωση**: Αφήνω αυτές τις επιλογές καθώς μπορείται να φτιάχνεται τα σκριπτάκια σας σε ένα από τα παραπάνω Text Editors και μετά απλά να τα τρέχεται μέσω του *pgAdmin*. Επίσης στην τελική εργασία θα πρέπει να χρησιμοποιήσεται *C++* ή *Java* ή *Python* ή γενικά όποια γλώσσα σας βολεύει για να κάνεται σύνδεση με την βάση σας, οπότε ένα Text Editor θα χρειαστεί.

<br />


## Websites

### Για τις εργασίες

* [Παραδείγματα εργαστηρίου](https://gunet2.cs.unipi.gr/modules/document/document.php?course=TMB102&openDir=/20100503182247ul704u6d/5e66b63cv1Zq) (Πρέπει να κάνετε **Login** πρώτα και να έχετε επιλέξει το μάθημα στο gunet2).
* [Official Documentation](https://www.postgresql.org/docs/13/index.html)
* [PostgreSQL Tutorial](https://www.postgresqltutorial.com/)
* [W3Schools SQL Tutorial](https://www.w3schools.com/sql/default.asp)
* [TutorialsPoint Learn SQL](https://www.tutorialspoint.com/sql/sql-syntax.htm)

**Σημείωση**: Δεν προτείνω τόσο το TutorialsPoint. Το πιο χρήσιμο για εμένα είναι το *Official Documention* που παρέχουν οι ίδιοι.

## Videos

### Για τις εργασίες

Δεν χρειάζεται κάποιο βίντεο tutorial για τις απαιτήσεις των εργασιών.
