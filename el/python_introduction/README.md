{% set warning_icon = '<span class="glyphicon glyphicon-exclamation-sign" style="color: red;" aria-hidden="true" data-toggle="tooltip" title="An error is expected when you run this command!" ></span>' %}

# Εισαγωγή στην Python

> Μέρος αυτού του κεφαλαίου είναι βασισμένο στους οδηγούς από την κοινότητα Geek Girls Carrots (https://github.com/ggcarrots/django-carrots).

Ας γράψουμε λίγο κώδικα!

## Παράθυρο εντολών Python

> Για τους αναγνώστες στο σπίτι: αυτό το μέρος που καλύπτεται από το βίντεο [Python Basics: Integers, Strings, Lists, Variables and Errors](https://www.youtube.com/watch?v=MO63L4s-20U).

Για να αρχίσετε να παίζετε με την Python, πρέπει να ανοίξετε μια *γραμμή εντολών* στον υπολογιστή σας. Πρέπει ήδη να ξέρετε πως το κάνουμε αυτό. Το μάθαμε στο κεφάλαιο [Εισαγωγή στη γραμμή εντολών](../intro_to_command_line/README.md).

Μόλις είστε έτοιμοι, ακολουθήστε τις παρακάτω οδηγίες.

Θέλουμε να ανοίξουμε μια κονσόλα Python. Πληκτρολογήστε `python` αν είστε σε Windows ή `python3` αν είστε σε Mac OS/Linux και πατήστε `enter`.

{% filename %}command-line{% endfilename %}

    $ python3
    Python 3.6.1 (...)
    Type "help", "copyright", "credits" or "license" for more information.
    >>>
    

## Η πρώτη σας Python εντολή!

Αφού εκτελέσετε την εντολή Python, το prompt θα αλλάξει σε `>>>`. Για εμάς αυτό σημαίνει ότι τώρα μπορεί να χρησιμοποιούμε μόνο εντολές για τη γλώσσα Python. Δεν χρειάζεται να πληκτρολογήσετε `>>>`. Θα το κάνει η Python για σας.

Εάν θέλετε να τερματίσετε την κονσόλα Python σε οποιοδήποτε σημείο, απλά πληκτρολόγηστε `exit()` ή `Ctrl + Z` για Windows και `Ctrl + D` για Mac/Linux. Τότε δεν θα μπορείτε να δείτε το `>>>` πια.

Για τώρα δεν θέλουμε να φύγουμε από αυτό το περιβάλλον. Θέλουμε να μάθουμε περισσότερα γι'αυτό. Ας ξεκινήσουμε να γράφουμε μερικές μαθηματικές πράξεις, όπως `2 + 3` και μετά πατάμε `enter`.

{% filename %}command-line{% endfilename %}

```python
>>> 2 + 3
5
```

Ωραία! Είδατε την απάντηση από κάτω; Η Python ξέρει μαθηματικά! Μπορείτε να δοκιμάσετε και άλλες εντολές, όπως:

- `4 * 5`
- `5 - 1`
- `40 / 2`

Για να εκτελέσετε εκθετικούς υπολογισμούς, πχ 2 στη δύναμη του 3, γράφουμε: {% filename %}command-line{% endfilename %}

```python
>>> 2 ** 3
8
```

Διασκέδασε με αυτό για λίγο και στη συνέχεια συνεχίστε πίσω εδώ. :)

Όπως μπορείτε να δείτε, η Python είναι μια πολύ καλή αριθμομηχανή. Αν αναρωτιέστε τι άλλο μπορείτε να κάνετε…

## Strings

Τι θα λέγατε για το όνομα σας; Πληκτρολογήστε το μικρό σας όνομα μέσα σε "αυτάκια", όπως παρακάτω:

{% filename %}command-line{% endfilename %}

```python
>>> "Ola"
"Ola"
```

Μόλις δημιουργήσατε το πρώτο σας string! Είναι μια ακολουθία χαρακτήρων η οποία επεξεργάζεται από τον υπολογιστή. Ένα string πρέπει πάντα να ξεκινά και να τελειώνει με τον ίδιο χαρακτήρα. Αυτό μπορεί να είναι είτε μονά "αυτάκια" (`'`) ή διπλά (`"`) (καμία διαφορά!). Τα "αυτάκια" λένε στην Python το εξής: ότι υπάρχει ανάμεσα θεώρησε το ως ένα string.

Τα strings μπορούν να ενωθούν. Δοκιμάστε το ακόλουθο:

{% filename %}command-line{% endfilename %}

```python
>>> "Hi there " + "Ola"
"Hi there Ola"
```

Μπορείτε επίσης να πολλαπλασιάσετε strings με αριθμό:

{% filename %}command-line{% endfilename %}

```python
>>> "Ola" * 3
'OlaOlaOla'
```

Αν χρειαστεί να βάλετε κάποια απόστροφο μέσα στο string, υπάρχουν δύο τρόποι να το κάνετε.

Χρησιμοποιώντας διπλά "αυτάκια":

{% filename %}command-line{% endfilename %}

```python
>>> "Runnin' down the hill"
"Runnin' down the hill"
```

ή κάνοντας escape την απόστροφο με ένα backslash (``):

{% filename %}command-line{% endfilename %}

```python
>>> 'Runnin\' down the hill'
"Runnin' down the hill"
```

Ωραίο εε; Για να δείτε το όνομα σας σε κεφαλαία, γράψτε:

{% filename %}command-line{% endfilename %}

```python
>>> "Ola".upper()
'OLA'
```

Μόλις χρησιμοποιήσατε την `upper` **method** πάνω στο string σας! Η μέθοδος (όπως η `upper()`) είναι μια ακολουθία από οδηγίες/εντολές που η Python πρέπει να εκτελέσει πάνω σε ένα συγκεκριμένο object (`"Ola"`) μόλις την καλέσετε.

Αν θέλετε να μάθετε τον αριθμό των γραμμάτων που περιέχονται στο όνομα σας, υπάρχει συνάρτηση **function** και γι'αυτό!

{% filename %}command-line{% endfilename %}

```python
>>> len("Ola")
3
```

Αναρρωτιέστε γιατί μερικές φορές καλείτε συναρτήσεις με την τελεία `.` στο τέλος ενός string (όπως `"Ola".upper()`) και άλλες καλείτε μια συνάρτηση και τοποθετείτε μέσα στις παρενθέσεις το string; Λοιπόν, σε κάποια σημεία οι συναρτήσεις ανήκουν σε objects, όπως η `upper()` η οποία επιδρά μόνο πάνω σε strings. Σε αυτή την περίπτωση, ονομάζουμε τις συναρτήσεις αυτές μεθόδους (**method**). Άλλες, πάλι, φορές οι συναρτήσεις δεν ανήκουν σε κάτι συγκεκριμένο και μπορούν να χρησιμοποιηθούν σε οποιουδήποτε τύπου object, όπως η `len()`. Γι'αυτό δίνουμε το string `"Ola"` ως παράμετρο στη συνάρτηση `len`.

### Περίληψη

Αρκετά με τα strings. Μέχρι τώρα μάθατε:

- **το prompt** – γράφοντας εντολές (κώδικα) μέσα σε περειβάλλον της Python έχει ως αποτέλεσμα να παίρνετε απαντήσεις από την Python
- **αριθμούς και strings** – στην Python οι αριθμοί χρησιμοποιούνται για μαθηματικά και τα strings για χαρακτήρες
- **operators** – όπως `+` και `*`, συνδυάζουν τιμές και παράγουν μια νέα τιμή
- **functions** – όπως η `upper()` και η `len()`, εκτελούν κάποιες ενέργειες στα objects.

Αυτά είναι τα βασικά για κάθε γλώσσα προγραμματισμού. Είστε έτοιμοι για κάτι πιο δύσκολο; Είμαστε σίγουροι ότι είστε!

## Σφάλματα

Ας δοκιμάσουμε κάτι καινούργιο. Μπορούμε να βρούμε το μήκος ενός αριθμού ακριβώς όπως κάναμε με το όνομα σας νωρίτερα; Πληκτρολογήστε `len(304023)` και πατήστε `enter`:

{% filename %}{{ warning_icon }} command-line{% endfilename %}

```python
>>> len(304023)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: object of type 'int' has no len()
```

Μόλις λάβατε το πρώτο σας σφάλμα! Το εικονίδιο {{ warning_icon }} είναι ο δικός μας τρόπος να σας πούμε ότι ο κώδικάς που πρόκειται να τρέξετε δεν θα έχει τα αναμενόμενα αποτελέσματα. Κάνοντας λάθη (ακόμα και εσκεμμένα) είναι σημαντικό κομμάτι κατά τη διάρκεια της εκμάθησης!

Το συγκεκριμένο σφάλμα λέει ότι τα objects τύπου "int" (από τη λέξη integers, που σημαίνει ακέραιοι αριθμοί) δεν έχουν μήκος. Οπότε τι κάνουμε τώρα; Μήπως να γράψουμε τον αριθμό ως ένα string; Τα strings έχουν μήκος, έτσι;

{% filename %}command-line{% endfilename %}

```python
>>> len(str(304023))
6
```

Δούλεψε! Χρησιμοποιήσαμε τη συνάρτηση `str` μέσα στην `len`. Η `str()` μετατρέπει τα πάντα σε strings.

- Η συνάρτηση `str` μετατρέπει πράγματα σε **strings**
- Η συνάρτηση `int` μετατρέπει πράγματα σε **integers**

> Σημαντικό: μπορούμε να μετατρέψουμε αριθμούς σε κείμενο (strings) αλλά όχι απαραίτητα το αντίστροφο. Τι θα συνέβαινε αν τρέχατε `int('hello')`;

## Μεταβλητές

Ένα σημαντικό έννοια στον προγραμματισμό είναι οι μεταβλητές. Μια μεταβλητή δεν είναι τίποτε άλλο από ένα όνομα που μπορεί να επαναχρησιμοποιηθεί αργότερα. Οι προγραμματιστές χρησιμοποιούν τις μεταβλητές για την αποθήκευση δεδομένων, κάνοντας τον κώδικα πιο ευανάγνωστο χωρίς να χρειάζεται να θυμούνται τι ήταν τι.

Ας υποθέσουμε ότι θέλετε να δημιουργήσετε μια μεταβλητή με το όνομα `name`:

{% filename %}command-line{% endfilename %}

```python
>>> name = "Ola"
```

Γράφουμε name ίσον με Ola.

Όπως θα παρατηρήσατε, το πρόγραμμα δεν επέστρεψε τίποτα όπως πριν. Πως ξέρουμε, λοιπόν, ότι η μεταβλητή υπάρχει; Πληκτρολογήστε`name` και μετά πιέστε `enter`:

{% filename %}command-line{% endfilename %}

```python
>>> name
'Ola'
```

Ναιιι! Η πρώτη σας μεταβλητή! :) Μπορείτε πάντα να αλλάξετε την τιμή αυτής της μεταβλητής:

{% filename %}command-line{% endfilename %}

```python
>>> name = "Sonja"
>>> name
'Sonja'
```

Μπορείτε να χρησιμοποιήσετε μεταβλητές σε συναρτήσεις:

{% filename %}command-line{% endfilename %}

```python
>>> len(name)
5
```

Φοβερό, έτσι; Οι μεταβλητές μπορεί να είναι οτιδήποτε (ακόμα και αριθμοί). Δοκιμάστε το εξής:

{% filename %}command-line{% endfilename %}

```python
>>> a = 4
>>> b = 6
>>> a * b
24
```

Αλλά τι θα γινόταν αν χρησιμοποιούσαμε λάθος όνομα; Τι θα συμβεί; Ας το δοκιμάσουμε!

{% filename %}{{ warning_icon }} command-line{% endfilename %}

```python
>>> city = "Tokyo"
>>> ctiy
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'ctiy' is not defined
```

Ένα σφάλμα! Όπως μπορείτε να δείτε, η Python έχει διαφορετικού τύπου σφάλματα (τα έχει κατατάξει σε κατηγορίες). Αυτό εδώ ονομάζεται **NameError**. Η Python θα σας εμφανίσει αυτό το σφάλμα αν προσπαθήσετε να χρησιμοποιήσετε κάποια μεταβλητή της οποίας το όνομα δεν έχει δηλωθεί. Αν εμφανίστηκε αυτό το σφάλμα νωρίτερα σε εσάς, δείτε τον κώδικά σας μήπως και έχετε κάνει λάθος σε κάποιο όνομα μεταβλητής.

Παίξτε για λίγο με αυτό και δείτε τι μπορείτε να κάνετε!

## Η συνάρτηση print

Δοκιμάστε αυτό:

{% filename %}command-line{% endfilename %}

```python
>>> name = 'Maria'
>>> name
'Maria'
>>> print(name)
Maria
```

Όταν απλώς πληκτρολογείτε `name`, η Python ανταποκρίνεται με το λεγόμενο string *representation* της τιμής της μεταβλητής 'name', η οποία είναι τα γράμματα M-a-r-i-a, περικυκλωμένα με τα μονά "αυτάκια", ''. Όταν λέτε `print(name)`, η Python θα "εκτυπώσει στην οθόνη" τα περιεχόμενα της μεταβλητής, χωρίς τα "αυτάκια", κάτι το οποίο είναι πιο ωραίο.

Όπως θα δούμε και αργότερα, η συνάρτηση `print()` είναι χρήσιμη όταν θέλουμε να εκτυπώσουμε πράγματα μέσα σε συναρτήσεις ή όταν θέλουμε να εκτυπώσουμε πράγματα σε πολλαπλές γραμμές αντί μιας.

## Λίστες

Πέρα από τα strings και τους αριθμούς, η Python προσφέρει αρκετά ακόμα διαφορετικούς τύπους objects. Παρακάωτ θα περιγράψουμε αυτό που αποκαλούμε λίστα (**list**). Οι λίστες είναι αυτό που φαντάζεστε: objects τα οποία είναι λίστες άλλων objects. :)

Πηγαίνετε και δημιουργήστε μια λίστα:

{% filename %}command-line{% endfilename %}

```python
>>> []
[]
```

Ναι, αυτή είναι μια κενή λίστα. Όχι πολύ χρήσιμη έτσι; Ας δημιουργήσουμε μια λίστα με αριθμούς. Δεν θέλουμε να επαναλαμβανόμαστε όλη την ώρα, οπότε θα βάλουμε τη λίστα μέσα σε μια μεταβλητή:

{% filename %}command-line{% endfilename %}

```python
>>> lottery = [3, 42, 12, 19, 30, 59]
```

Τέλεια, έχουμε μια λίστα! Τι μπορούμε να κάνουμε με αυτή; Ας δούμε πόσοι αριθμοί υπάρχουν μέσα στη λίστα. Ξέρετε, μήπως, ποια συνάρτηση μπορούμε να χρησιμοποιήσουμε γι'αυτό; Το ξέρετε ήδη!

{% filename %}command-line{% endfilename %}

```python
>>> len(lottery)
6
```

Ναι! Η συνάρτηση `len()` σας δίνει τον αριθμό των objects μέσα σε μια λίστα. Ωραίο, έτσι; Ίσως να μπορούμε να ταξινομήσουμε τους αριθμούς:

{% filename %}command-line{% endfilename %}

```python
>>> lottery.sort()
```

Αυτό δεν επιστρέφει τίποτα, απλώς άλλαξε τη σειρά με την οποία εμφανίζονται οι αριθμοί στη λίστα. Ας εκτυπώσουμε τη λίστα να δούμε πως άλλαξαν τα δεδομένα της:

{% filename %}command-line{% endfilename %}

```python
>>> print(lottery)
[3, 12, 19, 30, 42, 59]
```

Όπως βλέπετε, οι αριθμοί μέσα στη λίστα είναι πλέον ταξινομημένοι κατά αύξοντα αριθμό. Συγχαρητήρια!

Ίσως να θέλουμε να αντιστρέψουμε αυτή τη σειρά. Ας το κάνουμε!

{% filename %}command-line{% endfilename %}

```python
>>> lottery.reverse()
>>> print(lottery)
[59, 42, 30, 19, 12, 3]
```

Αν θέλετε να προσθέσετε κάτι στη λίστα σας, μπορείτε να το κάνετε με την ακόλουθη εντολή:

{% filename %}command-line{% endfilename %}

```python
>>> lottery.append(199)
>>> print(lottery)
[59, 42, 30, 19, 12, 3, 199]
```

Αν θέλετε να εμφανίσετε μόνο το πρώτο στοιχείο της λίστας, μπορείτε να το κάνετε χρησιμοποιώντας τα λεγόμενα **indexes**. Ένα index είναι ένας αριθμός ο οποίος δηλώνει σε ποιο σημείο ένα στοιχείο υπάρχει σε μια λίστα. Οι προγραμματιστές προτιμούν να ξεκινούν από το 0, οπότε το πρώτο στοιχείο θα βρίσκεται στη θέση (index) 0, το επόμενο στη θέση 1 κοκ. Δοκιμάστε αυτό:

{% filename %}command-line{% endfilename %}

```python
>>> print(lottery[0])
59
>>> print(lottery[1])
42
```

Όπως μπορείτε να δείτε, μπορείτε να έχετε πρόσβαση στα διαφορετικά στοιχεία μια λίστας γνωρίζοντας το όνομα της λίστας και τη θέση (index) του κάθε στοιχείου, δηλώνοντας το μέσα σε αγκύλες ([]).

Για να διαγράψετε κάτι από τη λίστα, θα χρειαστεί να χρησιμοποιήσετε τα **indexes** καθώς και την μέθοδο `pop()`. Δηλαδή, θα πρέπει να ξέρετε ποιο στοιχείο να διαγράψετε. Ας δοκιμάσουμε ένα παράδειγμα. Θα διαγράψουμε το πρώτο στοιχείο της λίστας.

{% filename %}command-line{% endfilename %}

```python
>>> print(lottery)
[59, 42, 30, 19, 12, 3, 199]
>>> print(lottery[0])
59
>>> lottery.pop(0)
59
>>> print(lottery)
[42, 30, 19, 12, 3, 199]
```

Δούλεψε μια χαρά!

Παίξτε λίγο παραπάνω: δοκιμάστε μερικές άλλες θέσεις (αριθμός μέσα στην αγκύλη) όπως 6, 7, 1000, -1, -6 ή -1000. Δείτε αν μπορείτε να προβλέψετε το αποτέλεσμα πριν πατήσετε enter. Συμφωνούν τα αποτελέσματα με την πρόβλεψη σας;

Μπορείτε να βρείτε την λίστα με όλες διαθέσιμες μεθόδους για μια λίστα στο Python documentation: https://docs.python.org/3/tutorial/datastructures.html

## Λεξικά

> Για τους αναγνώστες στο σπίτι: αυτή η ενότητα καλύπτεται στο βίντεο [Python Basics: Dictionaries](https://www.youtube.com/watch?v=ZX1CVvZLE6c).

Ένα λεξικό (dictionary ή όπως έχει επικρατήσει, dict εν συντομία) είναι όμοιο με μια λίστα αλλά έχετε πρόσβαση στις τιμές όχι κατά θέση (index) αλλά κατά ένα κλειδί (key). Ένα κλειδί μπορεί να είναι ένα string ή ένας αριθμός. Η σύνταξη για ένα κενό λεξικό είναι:

{% filename %}command-line{% endfilename %}

```python
>>> {}
{}
```

Αυτό σηλώνει ότι μόλις δημιουργήσατε ένα κενό dict. Συγχαρητήρια!

Τώρα, προσπαθήστε να εκτελέσετε την ακόλουθη εντολή (αντικαθιστώντας με δικά σας στοιχεία):

{% filename %}command-line{% endfilename %}

```python
>>> participant = {'name': 'Ola', 'country': 'Poland', 'favorite_numbers': [7, 42, 92]}
```

Με αυτή την εντολή μόλις δημιουργήσατε μια μεταβλητή με το όνομα `participant` με τρια ζευγάρια κλειδι-τιμή (key value pairs):

- Το πρώτο κλειδί είναι το `name` το οποίο αντιστοιχεί την τιμή `'Ola'` (είναι ένα `string` object),
- Το δεύτερο κλειδί με το όνομα `country` αντιστοιχεί στην τιμή `'Poland'` (άλλο ένα `string`),
- και το τρίτο κλειδί `favorite_numbers` αντιστοιχεί στην τιμή `[7, 42, 92]` (μια λίστα `list` με τρεις αριθμούς μέσα της).

Μπορείτε να δείτε τις τιμές κάθε κλειδιού με την ακόλουθη σύνταξη:

{% filename %}command-line{% endfilename %}

```python
>>> print(participant['name'])
Ola
```

Βλέπετε ότι είναι όμοια με μια λίστα. Απλώς δεν χριάζεται να θυμάστε τη θέση - μόνο το όνομα.

Τι θα συμβεί αν ζητήσουμε μια τιμή ενός κλειδιού η οποία δεν υπάρχει; Μπορείτε να μαντέψετε; Ας δοκιμάσουμε να δούμε!

{% filename %}{{ warning_icon }} command-line{% endfilename %}

```python
>>> participant['age']
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyError: 'age'
```

Είδατε, άλλο ένα σφάλμα το οποίο λέγεται **KeyError**. Η Python είναι αρκετά καλή σε αυτό. Δηλαδή στην περιγραφικότητα των σφαλμάτων της. Σας λέει ότι το κλειδί `'age'` δεν υπάρχει στο λεξικό.

Πότε πρέπει να χρησιμοποιείτε λεξικό έναντι μιας λίστας; Αυτό είναι ένα καλό ερώτημα. Σκεφτείτε λίγο την απάντηση πριν προχωρήσετε.

- Χρειάζεστε μια ταξινομημένη ακολουθία από στοιχεία; Η απάντηση είναι λίστα.
- Χρειάζεστε να συσχετίζετε κλειδιά ούτως ώστε να τα αναζητείτε αργότερα μόνο με το όνομα τους και όχι με τη θέση τους; Η απάντηση είναι dict.

Τα dicts όπως και οι λίστες είναι *mutable*, που σημαίνει ότι μπορούν να αλλάξουν μετά τη δημιουργία τους. Μπορείτε να προσθέσετε ένα νέο κλειδί-τιμή στο λεξικό αφού δημιουργηθεί, όπως παρακάτω:

{% filename %}command-line{% endfilename %}

```python
>>> participant['favorite_language'] = 'Python'
```

Όπως στις λίστες, χρησιμοποιώντας τη μέθοδο `len()` σε λεξικά, θα πάρετε τον αριθμό των ζευγαριών κλειδί-τιμή μέσα σε ένα λεξικό. Γράφτε το παρακάτω:

{% filename %}command-line{% endfilename %}

```python
>>> len(participant)
4
```

Ελπίζουμε να βγάζουν νόημα όλα αυτά μέχρι τώρα. :) Είστε έτοιμοι για περισσότερη διασκέδαση με τα λεξικά; Συνεχίστε να διαβάζετε για περισσότερα πράγματα που μπορείτε να κάνετε.

Μπορείτε να χρησιμοποιήσετε την μέθοδο `pop()` για να διαγράψετε ένα στοιχείο (ζευγάρι από κλειδί-τιμή) από ένα dict. Για παράδειγμα, αν θέλετε να διαγράψετε το ζευγάρι με το κλειδί `'favorite_numbers'`, γράψτε την ακόλουθη εντολή:

{% filename %}command-line{% endfilename %}

```python
>>> participant.pop('favorite_numbers')
[7, 42, 92]
>>> participant
{'country': 'Poland', 'favorite_language': 'Python', 'name': 'Ola'}
```

Όπως μπορείτε να δείτε από την έξοδο, το ζευγάρι του κλειδιού 'favorite_numbers' διαγράφηκε επιτυχώς.

Επίσης, μπορείτε να αλλάξετε την τιμή σε μια τιμή μέσα σε ένα λεξικό (αλλά όχι το ίδιο το κλειδί). Δοκιμάστε το εξής:

{% filename %}command-line{% endfilename %}

```python
>>> participant['country'] = 'Germany'
>>> participant
{'country': 'Germany', 'favorite_language': 'Python', 'name': 'Ola'}
```

Όπως βλέπετε, η τιμή του κλειδιού `'country'` αλλάξε από `'Poland'` σε `'Germany'`. :) Φοβερό έτσι; Μπράβο! Μόλις μάθατε άλλο ένα απίθανο πράγμα.

### Περίληψη

Τέλεια! Ξέρετε πολλά σχετικά με τον προγραμματισμό τώρα. Στην τελευταία ενότητα μάθατε τα εξής:

- **errors** – μάθατε πως να διαβάζετε και να καταλαβαινέτε τα σφάλματα τα οποία εμφανίζονται αν η Python δεν καταλαβαίνει κάποια εντολή που της δώσατε
- **variables** – ονόματα για objects τα οποία σας επιτρέπουν να γράφετε κώδικα πιο εύκολα αλλά και να είναι ο κώδικας σας πιο ευανάγνωστος
- **lists** – λίστες από objects που αποθηκεύονται σε μια συγκεκριμένη σειρά
- **dictionaries** – αντικείμενα τα οποία αποθηκεύονται υπό τη μορφή ζευγαριού κλειδί-τιμή

Ενθουσιασμένοι για το επόμενο μέρος; :)

## Σύγκριση πραγμάτων

> Για τους αναγνώστες στο σπίτι: αυτή η ενότητα καλύπτεται στο βίντεο [Python Basics: Comparisons](https://www.youtube.com/watch?v=7bzxqIKYgf4).

Ένα μεγάλος μέρος του προγραμματισμού περιλαμβάνει τη σύγκριση πραγμάτων. Ποιο είναι το πιο εύκολο πράγμα να συγκρίνουμε; Οι αριθμοί! Ας δούμε πως:

{% filename %}command-line{% endfilename %}

```python
>>> 5 > 2
True
>>> 3 < 1
False
>>> 5 > 2 * 2
True
>>> 1 == 1
True
>>> 5 != 2
True
```

Δώσαμε στην Python μερικούς αριθμούς προς σύγκριση. Όπως βλέπετε, όχι μόνο μπορεί να συγκρίνει αριθμούς αλλά και αποτελέσματα από μεθόδους. Καλό εε;

Αναρρωτιέστε γιατί βάλαμε `==` (δύο ίσον σύμβολα) για να εξακριβώσουμε αν οι αριθμοί είναι ίσοι; Χρησιμοποιούμε το μονό ίσον `=` για να αναθέσουμε μια τιμή σε μια μεταβλητή. Πάντα, **πάντα** θα χρειάζεται να βάζετε διπλό ίσον – `==` – αν θέλετε να δείτε αν δύο πράγματα είναι ίσα μεταξύ τους. Αν οι τιμές τους, δηλαδή, είναι ίδιες. Μπορούμε επίσης να εξακριβώσουμε αν οι τιμές τους δεν είναι ίσες. Γι'αυτό χρησιμοποιούμε το σύμβολο `!=`, όπως φαίνεται παραπάνω.

Ας δώσουμε στην Python δύο ακόμα εντολές:

{% filename %}command-line{% endfilename %}

```python
>>> 6 >= 12 / 2
True
>>> 3 <= 2
False
```

Είδαμε ότι τα σύμβολα `>` και `<`, αλλά τα ακόλουθα σύμβολα τι σημαίνουν: `>=`, `<=`; Διαβάστε τα κάπως έτσι:

- x `>` y σημαίνει: το x είναι μεγαλύτερο το y
- x `<` y σημαίνει: το x είναι μικρότερο του y
- x `<=` y σημαίνει: το x είναι μικρότερο ή ίσο του y
- x `>=` y σημαίνει: το x είναι μεγαλύτερο ή ίσο του y

Τέλεια! Θέλετε να δοκιμάσετε άλλο ένα; Δοκιμάστε αυτό:

{% filename %}command-line{% endfilename %}

```python
>>> 6 > 2 and 2 < 3
True
>>> 3 > 2 and 2 < 1
False
>>> 3 > 2 or 2 < 1
True
```

Μπορείτε να δώσετε στην Python όσα νούμερα θέλετε προς σύγκριση και θα σας δώσει την απάντηση! Πολύ καλό, έτσι;

- **and** – αν χρησιμοποιήσετε τον operator `and`, τότε και οι δύο συγκρίσεις θα πρέπει να είναι αληθείς (True) για να είναι όλη η εντολή True
- **and** – αν χρησιμοποιήσετε τον operator `or`, τότε αρκεί μόνο μια από τις συγκρίσεις να είναι αληθής (True) για να είναι όλη η εντολή True

Έχετε ακούσει την έκφραση "συγκρίνω μήλα με πορτοκάλια"; Ας το δοκιμάσουμε με την Python:

{% filename %}{{ warning_icon }} command-line{% endfilename %}

```python
>>> 1 > 'django'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: '>' not supported between instances of 'int' and 'str'
```

Όπως ισχύει με την παραπάνω έκφραση στην καθομιλουμένη, έτσι και στην Python δεν είναι δυνατόν να συγκριθεί ένας αριθμός (`int`) με ένα string (`str`). Αντ' αυτού, εμφανίζεται ένα σφάλμα τύπου **TypeError** το οποίο μας λέει ότι οι δύο τύποι objects δεν μπορούν να συγκριθούν μεταξύ τους.

## Λογικές τιμές

Χωρίς να το θέλετε, μόλις μάθατε έναν νέο τύπο object στην Python. Ονομάζεται **Boolean**.

Υπάρχουν μόνο δύο ειδών Boolean objects:

- True
- False

Αλλά για να το καταλάβει η Python θα πρέπει πάντα να το γράφετε ως 'True' (το πρώτο γράμμα κεφαλαίο με τα υπόλοιπα πεζά). Τα **true, TRUE, και tRUE δεν θα δουλέψουν – μόνο το True είναι σωστό.** (Το ίδιο ισχύει και για το 'False'.)

Τα booleans μπορούν να είναι και μεταβλητές! Δείτε εδώ:

{% filename %}command-line{% endfilename %}

```python
>>> a = True
>>> a
True
```

Μπορείτε να το κάνετε και έτσι:

{% filename %}command-line{% endfilename %}

```python
>>> a = 2 > 5
>>> a
False
```

Εξασκηθείτε και διασκεδάστε με τα Booleans δοκιμάζοντας τις ακόλουθες εντολές:

- `True and True`
- `False and True`
- `True or 1 == 1`
- `1 != 2`

Συγχαρητήρια! Τα Booleans είναι ένα από τα πιο διασκεδαστικά πράγματα στον προγραμματισμό και μόλις μάθατε πως να τα χρησιμοποιείτε!

# Αποθήκευση!

> Για τους αναγνώστες στο σπίτι: αυτή η ενότητα καλύπτεται στο βίντεο [Python Basics: Saving files and "If" statement](https://www.youtube.com/watch?v=dOAg6QVAxyk).

Τόση ώρα γράφαμε τον κώδικα στην κονσόλα η οποία μας περιορίζει στο να εισάγουμε μια γραμμή κάθε φορά. Τα περισσότερα προγράμματα αποθηκεύονται σε αρχεία και τρέχουν όταν τους ζητηθεί από τον **interpreter** ή τον **compiler** της αντίστοιχης γλώσσας προγραμματισμού. Τόση ώρα τρέχαμε τα προγράμματα μας σε μια γραμμή κάθε φορά μέσα στον Python **interpreter**. Θα χρειαστούμς περισσότερες από μια γραμμές κώδικα για τα επόμενα στάδια. Οπότε θα χρειαστεί εν συντομία να κάνουμε τα εξής:

- Να φύγουμε από τον Python interpreter
- Να ανοίξουμε τον επεξεργαστή κώδικα της αρέσκειας μας
- Να αποθηκεύσουμε κάποιο κομμάτι κώδικα σε ένα python αρχείο (με την κατάληξη .py)
- Να το τρέξουμε!

Για να φύγουμε από τον Python interpreter θα γράψουμε `exit()`

{% filename %}command-line{% endfilename %}

```python
>>> exit()
$
```

Αυτό θα σας επαναφέρει στη γραμμή εντολών.

Νωρίτερα, επιλέξαμε έναν επεξεργαστή κώδικα από την ενότητα [επεξεργαστής κώδικα](../code_editor/README.md). Θα χρειαστεί να ανοίξουμε τον επεξεργαστή κώδικα και να γράψουμε κώδικα σε ένα νέο αρχείο (ή αν χρησιμοποιείτε Chromebook, δημιουργήστε ένα νέο αρχείο μέσω του Cloud IDE και ανοίξτε το αρχείο):

{% filename %}editor{% endfilename %}

```python
print('Hello, Django girls!')
```

Προφανώς, είστε ένας αρκετά έμπειρος Python developer τώρα, οπότε γράφτε κάποιον κώδικα μέσα στο αρχείο.

Τώρα θέλουμε να αποθηκεύσουμε το αρχείο και να του δώσουμε ένα περιγραφικό όνομα. Ας το ονομάσουμς **python_intro.py** και ας το αποθηκεύσουμε στην επιφάνεια εργασίας. Μπορούμε να ονομάσουμε το αρχείο όπως θέλουμε αλλά το σημαντικό εδώ είναι η κατάληξηξ **.py** που πρέπει να έχει. Η κατάληξη **.py** λέει στο λειτουργικό μας σύστημα ότι αυτό το αρχείο αποτελεί ένα **εκτελέσιμο Python αρχείο** και έτσι η Python μπορεί να το τρέξει.

> **Σημείωση** Θα πρέπει να είδατε ήδη ένα από τα πιο ωραία πράγματα στους επεξεργαστές κώδικα: τα χρώματα! Στην Python κονσόλα, όλα ήταν το ίδιο χρώμα. Τώρα βλέπετε ότι η συνάρτηση `print` έχει διαφορετικό χρώμα από ένα string. Αυτό ονομάζεται "syntax highlighting" και είναι ένα πολύ χρήσιμο χαρακτηριστικό καθώς προγραμματίζετε. Τα χρώματα θα σας δίνουν βοήθεια, όπως ένα string που του λείπει ένα "αυτάκι" ή ένα τυπογραφικό λάθος (typo) σε κάποια λέξε κλειδί της Python όπως `def` κλπ). Αυτός είναι ένας λόγος που χρησιμοποιούμε έναν επεξεργαστή κώδικα. :) :)

Με αποθηκευμένο το αρχείο, είναι ώρα να το τρέξουμε! Χρησιμοποιώντας τις δεξιότητες που μάθατε στη γραμμή εντολών, χρησιμοποιήστε την κονσόλα για να **αλλάξετε φάκελο** και να μεταβείτε στην επιφάνεια εργασίας.

<!--sec data-title="Change directory: macOS" data-id="python_OSX"
data-collapse=true ces-->

Σε Mac, η εντολή θα μοιάζει κάπως έτσι:

{% filename %}command-line{% endfilename %}

    $ cd ~/Desktop
    

<!--endsec-->

<!--sec data-title="Change directory: Linux" data-id="python_linux"
data-collapse=true ces-->

Σε Linux, θα μοιάζει κάπως έτσι (η λέξη "Desktop" ίσως να είναι μεταφρασμένη στη γλώσσα σας ως "Επιφάνεια Εργασίας"):

{% filename %}command-line{% endfilename %}

    $ cd ~/Desktop
    

<!--endsec-->

<!--sec data-title="Change directory: Windows Command Prompt" data-id="python_windows" data-collapse=true ces-->

Στα Windows θα μοιάζει κάπως έτσι:

{% filename %}command-line{% endfilename %}

    > cd %HomePath%\Desktop
    

<!--endsec-->

<!--sec data-title="Change directory: Windows Powershell" data-id="python_windowsPSH" data-collapse=true ces-->

Και στα Windows Powershell, θα μοιάζει κάπως έτσι:

{% filename %}command-line{% endfilename %}

    > cd $Home\Desktop
    

<!--endsec-->

Αν κολλήσετε, ζητήστε βοήθεια. Για αυτόν ακριβώς το λόγο βρίσκονται οι βοηθοί!

Τώρα χρησιμοποιήστε την Python για να τρέξετε τον κώδικα στο αρχείο όπως κατώθι:

{% filename %}command-line{% endfilename %}

    $ python3 python_intro.py
    Hello, Django girls!
    

Σημείωση: στα Windows η εντολή 'python3' δεν αναγνωρίζεται. Αντ'αυτού χρησιμοποιήστε την εντολή 'python':

{% filename %}command-line{% endfilename %}

```python
> python python_intro.py
```

Τέλεια! Μόλις τρέξατε το πρώτο σας Python πρόγραμμα το οποίο είναι αποθηκευμένο σε αρχείο. Αισθάνεστε ωραία;

Μπορείτε, τώρα, να μεταβείτε σε ένα σημαντικό εργαλείο στον προγραμματισμό:

## If … elif … else

Μερικές φορές, πολλά πράγματα στον κώδικα θα πρέπει να εκτελούνται αν ισχύουν συγκεκριμένες συνθήκες. Γι'αυτό το λόγο η Python (και κάθε άλλη γλώσσα προγραμματισμού) έχει κάτι που ονομάζει **if statements**.

Αντικαταστήστε τον κώδικα στο αρχείο **python_intro.py** με αυτό:

{% filename %}python_intro.py{% endfilename %}

```python
if 3 > 2:
```

Αν το αποθηκεύσουμε και το τρέξουμε, θα δούμε το ακόλουθο σφάλμα:

{% filename %}{{ warning_icon }} command-line{% endfilename %}

    $ python3 python_intro.py
    File "python_intro.py", line 2
             ^
    SyntaxError: unexpected EOF while parsing
    

Η Python περιμένει από εμάς να της δώσουμε περαιτέρω οδηγίες για το τι θα γίνει (τι θα εκτελεστεί) αν η συνθήκε `3 > 2` είναι αληθής (ή αλλιώς `True`). Ας προσπαθήσουμε να εκτυπώσουμε τη λέξη "It works!". Αλλάξτε τον κώδικα στο αρχείο **python_intro.py** ως εξής:

{% filename %}python_intro.py{% endfilename %}

```python
if 3 > 2:
    print('It works!')
```

Παρατηρήστε ότι προσθέσαμε τέσσερα κενά (4 spaces) για να κάνουμε indent την τελευταία γραμμη. Πρέπει να το κάνουμε αυτό ούτως ώστε να πούμε στην Python τι να κάνει αν η συνθήκη είναι αληθής. Μπορείτε να βάλετε ένα διάστημα (έναν κενό χαρακτήρα) αλλά όλοι οι προγραμματιστές Python χρησιμοποιούν τέσσερα για να φαίνεται πιο όμορφο και ευανάγνωστο. Η χρήση του Tab λαμβάνεται ως 4 κενά αρκεί ο επεξεργαστής κώδικα να είναι ρυθμισμένος γι'αυτό. Όταν κάνετε την επιλογή σας (Tab ή κενοί χαρακτήρες), μην την αλλάξετε! Αν χρησιμοποιείτε τα 4 κενά τότε να χρησιμοποιείτε τα 4 κενά για πάντα. Αλλιώς θα προκύψουν προβλήματα (mixed Tabs and spaces).

Αποθηκεύστε το και δοκιμάστε να το ξανατρέξετε:

{% filename %}command-line{% endfilename %}

```python
$ python3 python_intro.py
It works!
```

Σημείωση: θυμηθείτε ότι στα Windows η εντολή 'python3' δεν αναγνωρίζεται. Χρησιμοποιείτε την 'python' για να τρέχετε αρχεία.

### Αν όμως η συνθήκη δεν είναι True;

Στα προηγούμενα παραδείγματα, ο κώδικας έτρεχε μόνο όταν η σνυθήκη ήταν αληθής. Αλλά η Python έχει και άλλα statements όπως το `elif` και το `else`:

{% filename %}python_intro.py{% endfilename %}

```python
if 5 > 2:
    print('5 is indeed greater than 2')
else:
    print('5 is not greater than 2')
```

Όταν αυτό τρέχει θα εκτυπώσει:

{% filename %}command-line{% endfilename %}

    $ python3 python_intro.py
    5 is indeed greater than 2
    

Αν το 2 ήταν μεγαλύτερο του 5 τότε η δεύτερη εντολή θα έτρεχε. Ας δούμε πως λειτουργεί η `elif`:

{% filename %}python_intro.py{% endfilename %}

```python
name = 'Sonja'
if name == 'Ola':
    print('Hey Ola!')
elif name == 'Sonja':
    print('Hey Sonja!')
else:
    print('Hey anonymous!')
```

και τρέξτε το:

{% filename %}command-line{% endfilename %}

    $ python3 python_intro.py
    Hey Sonja!
    

Είδατε τι έγινε εδώ; Το `elif` σας επέτρεψε να προσθέσετε έξτρα συνθήκες σε περίπτωση που οι προηγούμενες αποτύχουν.

Μπορείτε να προσθέσετε όσα `elif` θέλετε μετά το αρχικό `if`. Για παράδειγμα:

{% filename %}python_intro.py{% endfilename %}

```python
volume = 57
if volume < 20:
    print("It's kinda quiet.")
elif 20 <= volume < 40:
    print("It's nice for background music")
elif 40 <= volume < 60:
    print("Perfect, I can hear all the details")
elif 60 <= volume < 80:
    print("Nice for parties")
elif 80 <= volume < 100:
    print("A bit loud!")
else:
    print("My ears are hurting! :(")
```

Η Python τρέχει κάθε τεστ με τη σειρά και εκτυπώνει:

{% filename %}command-line{% endfilename %}

    $ python3 python_intro.py
    Perfect, I can hear all the details
    

## Σχόλια

Τα χόλια είναι γραμμές οι οποίοες ξεκινούν με την δίεση `#`. Μπορείτε να γράψετε ότι θέλετε μετά την δίεση `#` και πολύ απλά η Python θα το αγνοήσει. Τα σχόλια μπορούνα να κάνουν τον κώδικα σας πιο ευανάγνωστο σε άλλους προγραμματιστές και όχι μόνο.

Ας δούμε πως φαίνεται:

{% filename %}python_intro.py{% endfilename %}

```python
# Change the volume if it's too loud or too quiet
if volume < 20 or volume > 80:
    volume = 50
    print("That's better!")
```

Δεν χρειάζεται να γράφεται σχόλιο για κάθε γραμμή κώδικα (άλλωστε δεν είναι καλή πρακτική ούτως ή άλλως) αλλά τα σχόλια είναι χρήσιμα ως προς το να εξηγήσουν το τι κάνει ο κώδικας ή να δώσουν κάποιου είδους περίληψη όταν κάνετε κάτι περίπλοκο.

### Περίληψη

Στις τελευταίες ασκήσεις μάθατε τα εξής:

- **να συγκρίνετε πράγματα** – στην Python μπορείτε να συγκρίνετε πράγματα χρησιμοποιώντας `>`, `>=`, `==`, `<=`, `<` και `and`, `or`
- **Boolean** – ένας τύπος object το οποίο μπορεί να πάρει μόνο δύο τιμές: `True` ή `False`
- **Αποθήκευση αρχείων** – αποθήκευση κώδικα σε αρχεία ούτως ώστε να τρέχετε μεγαλύτερου όγκου προγράμματα.
- **if … elif … else** – αυτά τα statements σας επιτρέπουν να εκτελείτε κώδικα υπό συγκεκριμένες συνθήκες.
- **σχόλια** - γραμμές στην Python οι οποίες δεν εκτελούνται και σας επιτρέπουν να κάνετε τον κώδικα σας πιο περιγραφικό και ευανάγνωστο

Ώρα για το τελευταίο μέρος του κεφαλαίου!

## Οι δικές σας συναρτήσεις!

> Για τους αναγνώστες στο σπίτι: αυτή η ενότητα καλύπτεται στο βίντεο [Python Basics: Functions](https://www.youtube.com/watch?v=5owr-6suOl0).

Θυμάστε τις συναρτήσεις όπως τη `len()` που εκτελούσατε; Λοιπόν, σας έχουμε καλά νέα! Θα μάθετε πως να δημιουργείτε τις δικές σας!

Μια συνάρτηση είναι μια σειρά από οδηγίες που η Python πρέπει να εκτελέσει. Κάθε συνάρτηση ξεκινά με τη λέξη κλειδί της Python `def`, μετά ακολουθεί το όνομα αυτής και μετά δίνονται τυχόν παράμετροι. Ας το προσπαθήσουμε. Αντικαταστήστε τον κώδικα στο αρχείο **python_intro.py** με το ακόλουθο:

{% filename %}python_intro.py{% endfilename %}

```python
def hi():
    print('Hi there!')
    print('How are you?')

hi()
```

Ωραία. Η πρώτη μας συνάρτηση είναι έτοιμη!

Θα αναρρωτιέστε γιατί γράψαμε το όνομα της συνάρτησης στο τέλος του αρχείου. Αυτό γίνεται επειδή η Python διαβάζει το αρχείο και το τρέχει από την κορυφή έως το τέλος. Για να χρησιμοποιήσουμε, λοιπόν, την συνάρτηση μας θα πρέπει να την ξαναγράψουμε στο τέλος.

Ας το τρέξουμε για να δούμε το αποτέλεσμα:

{% filename %}command-line{% endfilename %}

    $ python3 python_intro.py
    Hi there!
    How are you?
    

Σημείωση: αν δεν δούλεψε, μην πανικοβάλεστε! Η έξοδος θα σας βοηθήσει να καταλάβετε το γιατί:

- Αν λέβετε ένα σφάλμα τύπου `NameError`, τότε ίσως γράψατε κάτι λάθος όπως το όνομα της συνάρτηση στο τέλος του αρχείου. Επιβεβαιώστε ότι το όνομα στη δήλωση της συνάρτηση `def hi():` είναι το ίδιο με το όνομα όταν την καλείτε `hi()`.
- Αν λάβατε ένα σφάλμα τύπου `IndentationError`, ελέγξτε ότι και οι γραμμές που καλούνται οι δύο συναρτήσεις `print` έχουν τον ίδιο αριθμό κενών στην αρχή: η Python απαιτεί όλος ο κώδικας μέσα στις συναρτήσεις να είναι στοιχισμένος το ίδιο.
- Αν δεν βλέπετε κάποια έξοδο τότε είτε έχετε παραλείψει να καλέσετε την συνάρτηση χρησιμοποιώντας τις παρενθέσεις `hi()` είτε το έχετε κάνει αλλά η κλήση της συνάρτησης (hi()) έχει *κενό* στην αρχή και αποτελεί μέρος του κυρίου σώματος της συνάρτησης (def hi():).

Ας φτιάξουμε την πρώτη μας συνάρτηση με παραμέτρους. Θα αλλάξουμε το προηγούμενο παράδειγμα συμπεριλαμβάνοντας ένα όνομα. Θα φτιάξουμε μια συνάρτηση που να λέει 'hi' στο πρόσωπο που την καλεί:

{% filename %}python_intro.py{% endfilename %}

```python
def hi(name):
```

Όπως βλέπετε, δώσαμε μια παράμετρο στην συνάρτηση με το όνομα `name`:

{% filename %}python_intro.py{% endfilename %}

```python
def hi(name):
    if name == 'Ola':
        print('Hi Ola!')
    elif name == 'Sonja':
        print('Hi Sonja!')
    else:
        print('Hi anonymous!')

hi()
```

Θυμηθείτε: Η συνάρτηση `print` είναι στοιχισμένη με 4 κενά μέσα στο statement `if`. Αυτό το κάνουμε διότι θέλουμε να εκτελεστεί η συνάρτηση όταν η συνθήκη στο if είναι αληθής. Ας δούμε πως δουλεύει τώρα:

{% filename %}{{ warning_icon }} command-line{% endfilename %}

    $ python3 python_intro.py
    Traceback (most recent call last):
    File "python_intro.py", line 10, in <module>
      hi()
    TypeError: hi() missing 1 required positional argument: 'name'
    

Ώπα, ένα σφάλμα. Ευτυχώς, η Python μας δίνει ένα αρκετά χρήσιμο σφάλμα. Μας λέει ότι η συνάρτηση `hi()` (αυτή που ορίσαμε) δέχεται μια απαραίτητη παράμετρο (με το όνομα `name`) και ότι ξεχάσαμε να την ορίσουμε καθώς την καλούσαμε. Ας το φτιάξουμε αυτό στο τέλος του αρχείου:

{% filename %}python_intro.py{% endfilename %}

```python
hi("Ola")
```

Και ας το τρέξουμε ξανά:

{% filename %}command-line{% endfilename %}

    $ python3 python_intro.py
    Hi Ola!
    

Και αν μπορούμε να αλλάξουμε το όνομα;

{% filename %}python_intro.py{% endfilename %}

```python
hi("Sonja")
```

Και το τρέξουμε:

{% filename %}command-line{% endfilename %}

    $ python3 python_intro.py
    Hi Sonja!
    

Τώρα τι νομίζετε ότι θα γίνει αν γράψετε άλλο όνομα εκεί μέσα; (Όχι το Ola ή το Sonja). Δοκιμάστε το και προβλέψτε την έξοδο. Θα εκτυπώσει το εξής:

{% filename %}command-line{% endfilename %}

    Hi anonymous!
    

Αυτό είναι φοβερό, έτσι; Με αυτό τον τρόπο δεν χρειάζεται να επαναλαμβάνεστε κάθε φορά που θέλετε να αλλάξετε το όνομα του προσώπου που η συνάρτηση υποτίθεται ότι χαιρετά. Και γι'αυτό το λόγο χρησιμοποιούμε τις συναρτήσεις. Δεν θέλετε ποτέ να επαναλάβετε τον κώδικα σας!

Ας κάνουμε κάτι πιο έξυπνο. Υπάρχουν περισσότερα ονόματα από δύο και το να γράφουμε συνθήκες για καθένα χωριστά καταντά κουραστικό και ευάλωτο σε λάθη. Αντικαταστήστε το περιεχόμενο του αρχείου σας με τα κατώθι:

{% filename %}python_intro.py{% endfilename %}

```python
def hi(name):
    print('Hi ' + name + '!')

hi("Rachel")
```

Ας τρέξουμε τον κώδικα τώρα:

{% filename %}command-line{% endfilename %}

    $ python3 python_intro.py
    Hi Rachel!
    

Συγχαρητήρια! Μόλις μάθατε πως να γράφετε συναρτήσεις! :)

## Επαναλήψεις

> Για τους αναγνώστες στο σπίτι: αυτή η ενότητα καλύπτεται στο βίντεο [Python Basics: For Loop](https://www.youtube.com/watch?v=aEA6Rc86HF0).

Αυτό είναι το τελευταίο κομμάτι. Ήταν σύντομο, έτσι; :)

Οι προγραμματιστές δεν θέλουν να επαναλαμβάνουν τα ίδια και τα ίδια. Ο προγραμματισμός έχει να κάνει με την αυτοματοποίηση των πραγμάτων. Οπότε δεν θέλουμε να χαιρετάμε κάθε πρόσωπο με το όνομα τους χειροκίνητα, έτσι; Εδώ, λοιπόν, έρχονται οι επαναλήψεις (ή loops ή βρόγχοι).

Θυμάστε τις λίστες; Ας φτιάξουμε μια λίστα με ονόματε κοριτσιών:

{% filename %}python_intro.py{% endfilename %}

```python
girls = ['Rachel', 'Monica', 'Phoebe', 'Ola', 'You']
```

Θέλουμε να τις χαιρετίσουμε όλες με το όνομα τους. Έχουμε, ήδη, μια συνάρτηση με το όνομα `hi`, οπότε θα χρησιμοποιήσουμε αυτή:

{% filename %}python_intro.py{% endfilename %}

```python
for name in girls:
```

Η λέξη κλειδί της Python `for` συμπεριφέρεται περίπου όπως το `if`. Το κυρίως σώμα του κώδικα που ακολουθεί θα πρέπει να είναι στοιχισμένο με 4 κενά.

Αυτός θα είναι ο κώδικας που θα υπάρχει στο αρχείο:

{% filename %}python_intro.py{% endfilename %}

```python
def hi(name):
    print('Hi ' + name + '!')

girls = ['Rachel', 'Monica', 'Phoebe', 'Ola', 'You']
for name in girls:
    hi(name)
    print('Next girl')
```

Και όταν το τρέχουμε:

{% filename %}command-line{% endfilename %}

    $ python3 python_intro.py
    Hi Rachel!
    Next girl
    Hi Monica!
    Next girl
    Hi Phoebe!
    Next girl
    Hi Ola!
    Next girl
    Hi You!
    Next girl
    

Όπως βλέπετε οτιδήποτε βάλτε μέσα σε ένα statement `for` με την ανάλογη στοίχιση θα επαναληφθεί για κάθε στοιχείο της λίστας `girls`.

Μπορείτε να χρησιμοποιήσετε το `for` και για αριθμούς χρησιμοποιώντας της συνάρτηση `range`:

{% filename %}python_intro.py{% endfilename %}

```python
for i in range(1, 6):
    print(i)
```

Το οποίο θα εκτυπώσει:

{% filename %}command-line{% endfilename %}

    1
    2
    3
    4
    5
    

Η συνάρτηση `range` δημιουργεί μια λίστα από αριθμούς (αυτοί οι αριθμοί εισάγονται από εσάς ως παράμετροι).

Σημειώστε ότι η δεύτερη παράμετρος δεν περιλαμβάνεται στην λίστα που επιστρέφει (δηλαδή το `range(1, 6)` θα μετρήσει από το 1 έως το 5, αλλά δεν θα συμπεριλάβει το 6). Αυτό γίνεται διότι η συνάρτηση "range" είναι τύπου κλειστό-ανοιχτό, δηλαδή συμπεριλαμβάνει την πρώτη τιμή αλλά όχι την τελευταία.

## Περίληψη

Αυτό ήταν. **Τα σπάτε!** Αυτό ήταν ένα δύσκολο κεφάλαιο, οπότε θα πρέπει να νιώθετε περίφανοι με τον εαυτό σας. Είμαστε πολύ περήφανοι που τα καταφέρατε μέχρι εδώ!

Για τον επίσημο και πλήρης Python οδηγό επισκεφτείτε την σελίδα https://docs.python.org/3/tutorial/. Αυτό θα σας δώσει μια πιο ολοκληρωμένη και εις βάθος γνώση αυτής της γλώσσας προγραμματισμού. Γεια σας :)

Ίσως θα θέλατε να κάνετε κάτι κάτι άλλο, πχ τεντωθείτε, να περπατήσετε λίγο, να ξεκουράσετε τα μάτια σας, πριν συνεχίσετε στο επόμενο κεφάλαιο. :)

![Κεκάκι](images/cupcake.png)