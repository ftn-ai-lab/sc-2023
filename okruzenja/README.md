# Okruženja za praktičan deo kursa

Za potrebe praktičnog dela kursa potrebno je instalirati [Python3](https://www.python.org/downloads/) (Python 3.10 ili 3.11) i odgovarajuće biblioteke. Spisak svih potrebnih biblioteka sa odgovarajućim verzijama se nalazi u: 
* **requirements.txt** fajlu ovog foldera repozitorijuma za *Linux/MacOS*  
* **requirements_win.txt** fajlu ovog foldera repozitorijuma za *Windows*.

Postoji nekoliko načina za instalaciju biblioteka i podešavanje odgovarajućeg okruženja,a na vama je da odaberete onaj koji Vam najviše odgovara:

## 1. "prosta" instalacija biblioteka  

#### Linux i MacOS

1) Iz ovog foldera repozitorijuma preuzeti **requirements.txt** fajl
2) Instalirati biblioteke (kroz *Terminal*):  
  a) `$ pip install -r requirements.txt` - ukoliko je na mašini instaliran samo jedan Python  
  b) `$ pip3.10 install -r requirements.txt` - ukoliko je na mašini instalirano više Python-a

#### Windows  

1) Iz ovog foldera preuzeti **requirements_win.txt** fajl  
2) Instalirati biblioteke (kroz *Command Prompt* ili *Powershell*):  
  a) `> pip install -r requirements_win.txt` - ukoliko je na mašini instaliran samo jedan Python  
  b) `> pip3.10 install -r requirements_win.txt` - ukoliko je na mašini instalirano više Pyt

## 2. Virtuelno okruženje  

[venv](https://docs.python.org/3/library/venv.html) je alat za kreiranje izolovanih (virtuelnih) Python okruženja. Vrši kreiranje okruženja koje ima sopstvene instalacione direktorijume, i koje ne deli pakete sa ostalim okruženjima (uključujući i globalno instalirane pakete).
Podešavanje i upotreba:

#### Linux i MacOS:  
  
1) U sklopu proizvoljnog foldera (preporuka da to bude folder repozitorijuma) kreirati virtuelno okruženje:  
`$ cd my_folder/`  
`$ python -m venv env` ili `$ python3.10 -m venv env` ili `$ python3.11 -m venv env`
2) Iz ovog foldera repozitorijuma preuzeti **requirements.txt** fajl, smestiti ga u folder gde ste kreirali virtuelno okruženje, aktivirati virtuelno okruženje i instalirati neophodne biblioteke:  
`$ source env/bin/activate`  
`$ pip install -r requirements.txt`  

Nakon izvrešenja poslednje komande, podešavanje virtuelnog okruženja je kompletirano i ono ostaje aktivno za (eventualni) dalji rad. 

Pre početka rada sa virtuelnim okruženjem, neophodno je pozicionirati se u folder u kom je kreiran i aktivirati ga:  
`$ cd my_folder/`  
`$ source env/bin/activate`  

Nakon završetka rada, virtuelno okruženje se deaktivira pomoću sledeće komande:  
`$ deactivate`  

Instalacija novog paketa u aktivno okruženje se vrši pomoću:  
`$ pip install ime_paketa`  

Ažuriranje liste instaliranih paketa u aktivnom okruženju (**requirements.txt**) se vrši pomoću komande:  
`$ pip freeze > requirements.txt`.  

#### Windows  

Na *Windows* operativnom sistemu podešavanja i upotreba su analogna podešavanju i upotrebi na *Linux* i *MacOS* operativnim sistemima. Jedina razlika jeste prilikom aktiviranja i deaktiviranja okruženja.  
Prilikom kreiranja okruženja za *Windows* operativnom sistemu se kreiraju aktivacione skripte za *Command Prompt* i *Powershell*, te se zbog toga aktivacija okruženja na *Windows*-u vrši pomoću komande:  
`> \path\to\env\Scripts\activate`  
Deaktivacija se vrši pomoću komande:  
`> deactivate`

## 3. Samostalna instalacija biblioteka  

Ukoliko *pip* ne može da instalira sve biblioteke iz **requirements.txt** ili **requirements_win.txt** onda je potrebno biblioteke samostalno instalirati pomoću komande:  
```bash
$ pip install numpy scipy matplotlib pandas scikit-learn tensorflow opencv-python notebook librosa
```

## 4. Anaconda  

[Anaconda Individual Edition](https://www.anaconda.com/) predstavlja *open source* distribuciju za rad sa *AI*-om i *Data Science*-om u programskim jezicima *R* i *Python* na *Linux*, *Windows* i *MacOS* operativnim sistemima. Predstavlja industrijski standard za razvoj, testiranje i trening na jednom računaru.  

Uputstva za instalaciju:  
* [Linux](https://docs.anaconda.com/anaconda/install/linux/)  
* [MacOS](https://docs.anaconda.com/anaconda/install/mac-os/)
* [Windows](https://docs.anaconda.com/anaconda/install/windows/)

Korisničku dokumentaciiju možete pronaći [ovde](https://anaconda.cloud/support-center).
