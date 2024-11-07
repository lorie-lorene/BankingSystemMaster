
# MISE EN PLACE D’UNE APPLICATION MICROSERVICE DE SERVICE BANCAIRE( ORANGE – MTN )
          ## BankingSystemMaster

SITUATION PROBLEME:

	Dans une plateforme, des utilisateurs aimeraient souscrire a des services financiers tels que les depots d’argent , les retraits d’argent, etc.. pour cela, on leur a demande d’addresser une demande de creation de compte dans une agence a laquelle ils sont affilies. De ce fait , la creation d’un utilisateur sera une demande envoye dans une agence, cette agence devra retransferer la dite demande dans le service approprie afin de verifier les informations qui sont dans la demande… le service aura le choix de valider la demande ou de la decliner :

– en cas de validation, le service qui  a valide la demande, enverra la reponse a l’agence en question, qui en suite se chargera de créer le compte de l’utilisateur correspondant. Le compte cree , l’utilisateur sera informe de cela a travers un service d’annonce.

-- en cas de declinaison, le service qui  a refuse la demande, envoyera la reponse a l’agence en question, qui en suite se chargera tranferer la reponse negative a l’utilisateur correspondant avec le motif de reuf. l’utilisateur sera informe de cela a travers un service d’annonce.

TECHNOLOGIES DE BASES
	**Communication:  Architecture pilote par evenement cas de rabbitMq 
	**Base de donnee evenementielle: cas de  EventStore
	**Base de donne relationelle : H2 ou Mysql
	**architecture d’implementation : Spring cloud


SERVICE DE BASES:

-service de configuration ( service-config) 
-service de registration ( service-registry) 
-service d’equilibrage de charge ( service-gateway) 
-service de tolerance de panne ( service-breaker) 

SERVICES DE L’APPLICATION ( Fonctionnalites)




