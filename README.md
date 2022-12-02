# Base-de-dades

-----------------------------------------------------Exercici 1-------------------------------------------------------------------

El DB conté informació de pel·lícules com el títol, el gènere, la persona amb la data I el lloc de naixement així com el de defunció en el cas que hi hagués, el rol al qual fa referència aquesta persona com podrien ser actor, guionista, etc.. així com si la pel.licula ha obtingut un premi.

Hi ha cinc taules que es distribueixen de la següent manera:

- la taula "genere" amb 11 entrades 
- la taula "movie" amb 16 entrades 
- la taula "movie person" amb 50 entrades
- la taula "person" amb 42 entrades
- la taula "role" amb 5 entrades 

La taula "movie" i "genere"estan relacionades entre si perquè la primera conte un camp que indica el "genere" de la pel·lícula.

La taula "movie person" esta relacionada amb les taules "person", "rol " i “movie” ja que "movie person" conté els ids d’aquestes taules.


----------------------------------------------------- Exercici 2 --------------------------------------------------------------------------------

SELECT person_name, person_country, person_dob from tb_person WHERE person_dod IS NULL ORDER BY person_dob ASC;

----------------------------------------------------- Exercici 3 --------------------------------------------------------------------------------

SELECT count(movie_genre_id), movie_title, movie_genre_id, genre_name FROM tb_movie 
INNER JOIN tb_genre 
ON movie_genre_id = genre_id 
GROUP BY movie_genre_id
ORDER BY count(movie_genre_id) DESC;

----------------------------------------------------- Exercici 4 --------------------------------------------------------------------------------

----------------------------------------------------- Exercici 5 --------------------------------------------------------------------------------

INSERT INTO tb_genre (genre_id, genre_name, created_by_user)
VALUES (69, 'Documental', 'Diana');


----------------------------------------------------- Exercici 6 --------------------------------------------------------------------------------

  delete from tb_movie_person where movie_id = 11;
  delete from tb_movie where movie_name = 'La Gran Familia Española';

----------------------------------------------------- Exercici 7 --------------------------------------------------------------------------------
