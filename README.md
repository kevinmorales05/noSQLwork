Examen del Primer Bimestre
Nombre: Kevin Morales
Fecha: 2021/07/30

Parte 1
•	Script Ejercicio 1 ORLANDO
#Orlando Juegos Olimpicos
import couchdb
from tweepy import Stream
from tweepy import OAuthHandler
from tweepy.streaming import StreamListener
import json

###API ########################
ckey = "C8gYxcJRD2ZuuQ2hnBKJvZzZm"
csecret = "I7RuUZi6VSKLZsLV0qwPjQK1Xmwf95FQPTdiMua6I21aCVfrwV"
atoken = "3550065256-xxGrQDuYC4YrDNtFNchfSyetoFmnhz4mjIhdnMh"
asecret = "99Wxr7Y4S5zpM4DRmnAYMiyd5qoWbypgypgXXc9bLx0LN"
#####################################

class listener(StreamListener):
    
    def on_data(self, data):
        dictTweet = json.loads(data)
        try:
            
            dictTweet["_id"] = str(dictTweet['id'])
            doc = db.save(dictTweet)
            print ("SAVED" + str(doc) +"=>" + str(data))
        except:
            print ("Already exists")
            pass
        return True
    
    def on_error(self, status):
        print (status)
        
auth = OAuthHandler(ckey, csecret)
auth.set_access_token(atoken, asecret)
twitterStream = Stream(auth, listener())

'''========couchdb'=========='''
server = couchdb.Server('http://kevin:12345@localhost:5984/')  #('http://115.146.93.184:5984/')
try:
    db = server.create('juegosolimpicos2')
except:
    db = server['juegosolimpicos2']
    
'''===============LOCATIONS=============='''    

twitterStream.filter(locations=[-81.409221,28.510477,-81.324077,28.561631])  
twitterStream.filter(track=['juegosolimpicos','carapaz'])

•	Script Ejercicio 1 QUITO
#Quito Juegos Olimpicos
import couchdb
from tweepy import Stream
from tweepy import OAuthHandler
from tweepy.streaming import StreamListener
import json

###API ########################
ckey = "C8gYxcJRD2ZuuQ2hnBKJvZzZm"
csecret = "I7RuUZi6VSKLZsLV0qwPjQK1Xmwf95FQPTdiMua6I21aCVfrwV"
atoken = "3550065256-xxGrQDuYC4YrDNtFNchfSyetoFmnhz4mjIhdnMh"
asecret = "99Wxr7Y4S5zpM4DRmnAYMiyd5qoWbypgypgXXc9bLx0LN"
#####################################

class listener(StreamListener):
    
    def on_data(self, data):
        dictTweet = json.loads(data)
        try:
            
            dictTweet["_id"] = str(dictTweet['id'])
            doc = db.save(dictTweet)
            print ("SAVED" + str(doc) +"=>" + str(data))
        except:
            print ("Already exists")
            pass
        return True
    
    def on_error(self, status):
        print (status)
        
auth = OAuthHandler(ckey, csecret)
auth.set_access_token(atoken, asecret)
twitterStream = Stream(auth, listener())

'''========couchdb'=========='''
server = couchdb.Server('http://kevin:12345@localhost:5984/')  #('http://115.146.93.184:5984/')
try:
    db = server.create('juegosolimpicos3')
except:
    db = server['juegosolimpicos3']
    
'''===============LOCATIONS=============='''    

twitterStream.filter(locations=[-78.527042,-0.264936,-78.486942,-0.199842])  
twitterStream.filter(track=['juegosolimpicos','carapaz'])

•	Script Ejercicio 1 GUAYAQUIL

#Guayaquil Juegos Olimpicos
import couchdb
from tweepy import Stream
from tweepy import OAuthHandler
from tweepy.streaming import StreamListener
import json

###API ########################
ckey = "C8gYxcJRD2ZuuQ2hnBKJvZzZm"
csecret = "I7RuUZi6VSKLZsLV0qwPjQK1Xmwf95FQPTdiMua6I21aCVfrwV"
atoken = "3550065256-xxGrQDuYC4YrDNtFNchfSyetoFmnhz4mjIhdnMh"
asecret = "99Wxr7Y4S5zpM4DRmnAYMiyd5qoWbypgypgXXc9bLx0LN"
#####################################

class listener(StreamListener):
    
    def on_data(self, data):
        dictTweet = json.loads(data)
        try:
            
            dictTweet["_id"] = str(dictTweet['id'])
            doc = db.save(dictTweet)
            print ("SAVED" + str(doc) +"=>" + str(data))
        except:
            print ("Already exists")
            pass
        return True
    
    def on_error(self, status):
        print (status)
        
auth = OAuthHandler(ckey, csecret)
auth.set_access_token(atoken, asecret)
twitterStream = Stream(auth, listener())

'''========couchdb'=========='''
server = couchdb.Server('http://kevin:12345@localhost:5984/')  #('http://115.146.93.184:5984/')
try:
    db = server.create('juegosolimpicos5')
except:
    db = server['juegosolimpicos5']
    
'''===============LOCATIONS=============='''    

#twitterStream.filter(locations=[-79.933971,-2.207867,-79.852672,-2.110707])  
twitterStream.filter(track=['juegosolimpicos','carapaz'])

 
Parte 2
•	Script Ejercicio 2
import couchdb
from tweepy import Stream
from tweepy import OAuthHandler
from tweepy.streaming import StreamListener
import json

###API ########################
ckey = "C8gYxcJRD2ZuuQ2hnBKJvZzZm"
csecret = "I7RuUZi6VSKLZsLV0qwPjQK1Xmwf95FQPTdiMua6I21aCVfrwV"
atoken = "3550065256-xxGrQDuYC4YrDNtFNchfSyetoFmnhz4mjIhdnMh"
asecret = "99Wxr7Y4S5zpM4DRmnAYMiyd5qoWbypgypgXXc9bLx0LN"
#####################################

class listener(StreamListener):
    
    def on_data(self, data):
        dictTweet = json.loads(data)
        try:
            
            dictTweet["_id"] = str(dictTweet['id'])
            doc = db.save(dictTweet)
            print ("SAVED" + str(doc) +"=>" + str(data))
        except:
            print ("Already exists")
            pass
        return True
    
    def on_error(self, status):
        print (status)
        
auth = OAuthHandler(ckey, csecret)
auth.set_access_token(atoken, asecret)
twitterStream = Stream(auth, listener())

'''========couchdb'=========='''
server = couchdb.Server('http://kevin:12345@localhost:5984/')  #('http://115.146.93.184:5984/')
try:
    db = server.create('juegosolimpicos')
except:
    db = server['juegosolimpicos']
    
'''===============LOCATIONS=============='''    

#twitterStream.filter(locations=[11.4037,41.7901,13.9414,43.568])  
twitterStream.filter(track=['juegosolimpicos','carapaz'])
 


PARTE 5
Se instala la dependencia de tiktok scraper en un proyecto de node.js:
 npm i -g tiktok-scraper

 
Fuente 1
•	Con este comando bajo la información en csv de 100 videos del tiktoker
tiktok-scraper user f.musicas -t 'csv' -n 100 --session sid_tt=dae32131231
 
Fuente 2
•	Con este comando bajo la información en csv de 100 videos del tiktoker
tiktok-scraper user pollosus -t 'csv' -n 100 --session sid_tt=dae32131231
 
Con esto ya se tiene 2 archivos en csv para trabajar con MongoDB.
Parte 6
Importación a la base de datos SQL Lite
Se procedió a abrir el programa DB Browser.
En File, escojo Import y el tipo de archivo CSV
 
Escojo pollosus, el csv creado del tiktoker con el mismo nombre
 
Hago click en Open y la información se despliega en la siguiente tabla:
Click en OK, y ya se importó el csv como una tabla en la base de datos
 
Repito lo mismo para agregar los otros datos del otro tiktoker, para que el nombre del campo salga con el nombre original se debe hacer click en el check de ‘Columns names in first line’ 
Con esto ya se tiene la base de datos en SQL LITE
 
Se realiza el mismo proceso con f.musicas
 
Realizo una consulta de ejemplo en el motor sql, en la tabla f, y se demuestra el correcto funcionamiento.
 

Parte 6
Exportar los archivos CSV tomados de la base de datos de DB Browser a MongoDB.
En DB Browser escojo exportar a csv.
 
Escojo las tablas a Exportar
 
Escojo el lugar donde almacenar y click en Select Folder.
 
En Mongo DB Compass
En el localhost creo una base de datos
 
En la colección tiktokers hago click en importar archivos
 
Escojo el formato csv
 
Click en Open, escojo formato CSV, e importo
 
Listo, con esto ya está importada la información.

 
Importo la otra fuente
 
En total se tienen 128 ingresos.
Totalmente comprobado:
 
PARTE 7

PARTE 8
Escojo exportar toda la colección
 
Escojo todos los campos
 
Luego selecciono el output
 
Luego exporto y tomo ese archivo para subirlo al servidor de MongoDB Atlas.
Conecto MongoDB Compass , y procedo a crear una base de datos en el Cluster creado para este propósito.
 
Creo una base de datos
 
Importo la base de datos, para ello entro en info para luego subir los datos
 
Escojo tiktokers
 
El archivo proveniente de MongoDB está ahora en MongoDB Atlas.
 
Los documentos están en Atlas ahora
 
Se procede a abrir MongoDB Atlas para verificar todo el trabajo realizado. En MongoDB Atlas escojo Collections para ver todas las colecciones. En tiktokData puedo ver a tiktokers, con sus 128 documentos.
 
Ahora despliego la información para ver todo.
 



