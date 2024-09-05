## Selezionare tutti gli eventi gratis, cioè con prezzo nullo (19)
soluzione: SELECT * FROM `events` WHERE price IS NULL;
## Selezionare tutte le location in ordine alfabetico (82)
soluzione: SELECT * FROM `locations` ORDER BY name ASC;
## Selezionare tutti gli eventi che costano meno di 20 euro e durano meno di 3 ore (38)
soluzione: SELECT * FROM `events` WHERE price < 20 AND duration < '02:59:00%';
## Selezionare tutti gli eventi di dicembre 2023 (25)
soluzione: SELECT * FROM `events` WHERE start LIKE '2023-12%';
## Selezionare tutti gli eventi con una durata maggiore alle 2 ore (823)
soluzione: SELECT * FROM `events` WHERE duration > '02:59:00%';
## Selezionare tutti gli eventi, mostrando nome, data di inizio, ora di inizio, ora di fine e durata totale (1040)
soluzione: SELECT name,start,duration,end_of_sale FROM `events`;
## Selezionare tutti gli eventi aggiunti da “Fabiano Lombardo” (id: 1202) (132)
soluzione: SELECT * FROM `events` WHERE user_id = '1202%';
## Selezionare il numero totale di eventi per ogni fascia di prezzo (81)
soluzione: SELECT COUNT(*) FROM `events` GROUP BY price;
## Selezionare tutti gli utenti admin ed editor (9)
soluzione: SELECT * FROM `users` WHERE role_id LIKE 1 OR role_id LIKE 2;
## Selezionare tutti i concerti (eventi con il tag “concerti”) (72)
soluzione: SELECT * FROM `event_tag` WHERE tag_id = 1;
## Selezionare tutti i tag e il prezzo medio degli eventi a loro collegati (11)
soluzione: SELECT * FROM `tags` INNER JOIN `events` ON `events`.`price`;
## Selezionare tutte le location e mostrare quanti eventi si sono tenute in ognuna di esse (82)
soluzione: SELECT * FROM `locations` INNER JOIN `events`;
## Selezionare tutti i partecipanti per l’evento “Concerto Classico Serale” (slug: concerto-classico-serale, id: 34) (30)
soluzione: SELECT * FROM `bookings` WHERE event_id = 34; 