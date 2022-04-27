# p-ags_religionsgemeinschaften

## Schema-Jobs

Branch: `ags_religionsgemeinschaften `

Edit:
```
./start-gretl.sh --docker-image sogis/gretl:latest --docker-network schema-jobs_default --topic-name ags_religionsgemeinschaften --schema-dirname schema createRolesDevelopment

./start-gretl.sh --docker-image sogis/gretl:latest --docker-network schema-jobs_default --topic-name ags_religionsgemeinschaften --schema-dirname schema createSchema configureSchema grantPrivileges

./start-gretl.sh --docker-image sogis/gretl:latest --docker-network schema-jobs_default --topic-name ags_religionsgemeinschaften --schema-dirname schema dropSchema
```

```
java -jar /Users/stefan/apps/ili2pg-4.3.1/ili2pg-4.3.1.jar --dbhost localhost --dbport 54321 --dbdatabase edit --dbusr ddluser --dbpwd ddluser --dbschema ags_religionsgemeinschaften_v1 --models SO_AGS_Religionsgemeinschaften_20220422 --export fubar_edit.xtf
```


Pub:
```
./start-gretl.sh --docker-image sogis/gretl:latest --docker-network schema-jobs_default --topic-name ags_religionsgemeinschaften --schema-dirname schema_pub createRolesDevelopment

./start-gretl.sh --docker-image sogis/gretl:latest --docker-network schema-jobs_default --topic-name ags_religionsgemeinschaften --schema-dirname schema_pub createSchema configureSchema grantPrivileges

./start-gretl.sh --docker-image sogis/gretl:latest --docker-network schema-jobs_default --topic-name ags_religionsgemeinschaften --schema-dirname schema_pub dropSchema
```

```
java -jar /Users/stefan/apps/ili2pg-4.3.1/ili2pg-4.3.1.jar --dbhost localhost --dbport 54322 --dbdatabase pub --dbusr ddluser --dbpwd ddluser --dbschema ags_religionsgemeinschaften_pub_v1 --models SO_AGS_Religionsgemeinschaften_Publikation_20220427 --export fubar_pub.xtf
```

## Gretl-Job

Branch: `master`

```
./start-gretl.sh --docker-image sogis/gretl:latest --docker-network schema-jobs_default --job-directory $PWD/ags_religionsgemeinschaften_pub 

```


### Symbole:

SVG-Symbole immer weiss ausgefüllt. Hintergrund gemäss Auflistung. Grösse Hintergrund circa 12mm. Umrandung weiss circa 1mm. Grösse SVG circa 6.6mm (muss man rumspiele). Eventuell bissle Offset setzen.

- Islam: #4e9027 / star-and-crescent-solid.svg
- Alevitentum: #502792 / ???
- Christentum: #00559B / cross-solid.svg
- Hinduismus: #F97D00 / om-solid.svg
- Buddhismus: #FCEA00 / dharmachakra-solid.svg
- Sikh: #FF4F42 / khanda-solid.svg
- Baha'i: #737373 / bahai-solid.svg
- Antroposophie: #9D17B0 / place-of-worship-solid.svg

