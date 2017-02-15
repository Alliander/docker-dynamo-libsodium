## Docker image voor standaard image met Libsodium

Libsodium is een en-/decryptie library die in USEF gebruikt wordt om berichten de coderen en decoderen.

Het maken/update van de image doe je met:
```console
$ docker build -t usefdynamo/libsodium:0.1 .
```

Om dit image beschikbaar te hebben in de k8s omgeving(en) moet het nog gepushed worden naar de usefdynamo repository:
```console
$ docker push usefdynamo/libsodium:0.1
```

*Check het versie nummer voordat je bovenstaande commando's uitvoert! De bedoeling is dat deze repo automatisch gebouwd gaat worden middels Docker Hub of Quay.io. Op dit moment is het nog niet zover en moeten wijzigingen in deze repo's handmatig gepushed worden.*