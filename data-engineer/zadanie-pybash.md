**Opis**

Przyjrzyj się poniższej sesji w terminalu i odpowiedz na trzy pytania.

```
$ virtualenv venv1
New python executable in /Users/szymon/gcp/venv1/bin/python
Installing setuptools, pip, wheel...done.
$ source venv1/bin/activate
$ python -c "import jupyter"
Traceback (most recent call last):
  File "<string>", line 1, in <module>
ImportError: No module named jupyter
$ 
$ echo $?
1
$ echo $?
0
$ !545
$ python -c "import jupyter"
$ history | grep 545
<co tu jest 1>
$ pip freeze > requirements.txt
$ cat requirements.txt | <co tu jest 2> | awk -F'-' '{print $1}' | sort | uniq -c
...
 1 html5lib
 1 ipykernel
 2 ipython
 1 ipywidgets
 1 jsonschema
 4 jupyter
...
```
**Pytania**

1. Dlaczego komenda `echo $?` zwraca czasem 1 a innym razem 0
2. Co według Ciebie jest w wyniku komendy oznaczonym jako <co tu jest 1>
3. Co według Ciebie jest w fragmencie komendy oznaczonym jako <co tu jest 2>

**Powodzenia!**
