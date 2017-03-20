# SQL Homework Questions

Use the supplied data as the source of data to answer the questions.  Copy the SQL command you have used to get the answer, and paste it below the question, along with the result they gave.

## Questions

1. Return ALL the data in the 'movies' table.
  select * from movies;

    1 | Iron Man                            | 2008 | 21:00
    2 | The Incredible Hulk                 | 2008 | 14:20
    3 | Iron Man 2                          | 2010 | 18:45
    4 | Thor                                | 2011 | 22:20
    5 | Captain America: The First Avenger  | 2011 | 16:45
    6 | Avengers Assemble                   | 2012 | 21:05
    7 | Iron Man 3                          | 2013 | 17:30
    8 | Thor: The Dark World                | 2013 | 14:30
    9 | Batman Begins                       | 2005 | 20:00
   10 | Captain America: The Winter Soldier | 2014 | 23:25
   11 | Guardians of the Galaxy             | 2014 | 17:40
   12 | Avengers: Age of Ultron             | 2015 | 23:40
   13 | Ant-Man                             | 2015 | 16:35
   14 | Captain America: Civil War          | 2016 | 23:40
   15 | Doctor Strange                      | 2016 | 23:30
  (15 rows)


2. Return ONLY the name column from the 'people' table
  select name from people;

  Paule Akramaitė-Dean
   Reece Baird
   Rhys Brame
   James Duncan
   Dominic Fraser
   Euan Fullarton
   Eden Graham
   Tristan Gray
   Zsolt Podoba-Szalai
   instructor
   instructor
   Andrew Gurney
   Caroline Hatwell
   jhn Harper
   Duncan Henderson
   Benjamin Kinnard
   Allegra Perazzo
   Rajini Poosa
   William Proudfoot
   David Robertson
   Michael Shennan
   Ian Tennyson
   Eun-joo Yoon


3.Oops! Someone at CodeClan spelled John's name wrong! Change it to reflect the proper spelling (change 'jhn Harper' to 'John Harper').
  UPDATE people SET name = "John Harper" WHERE name = "jhn Harper";

  Paule Akramaitė-Dean
   Reece Baird
   Rhys Brame
   James Duncan
   Dominic Fraser
   Euan Fullarton
   Eden Graham
   Tristan Gray
   Zsolt Podoba-Szalai
   instructor
   instructor
   Andrew Gurney
   Caroline Hatwell
   Duncan Henderson
   Benjamin Kinnard
   Allegra Perazzo
   Rajini Poosa
   William Proudfoot
   David Robertson
   Michael Shennan
   Ian Tennyson
   Eun-joo Yoon
   John Harper
  (23 rows)


4. Return ONLY your name from the 'people' table.

  select name from people where name = 'Eden Graham';

  -------------
   Eden Graham
  (1 row)

5. The cinema is showing 'Batman Begins', but Batman is DC, not Marvel! Delete the entry from the 'movies' table.

  DELETE FROM movies WHERE title = 'Batman Begins';

  DELETE 1


6. Create a new entry in the 'people' table with the name of one of the other instructors (Tony, Kat, etc).

  INSERT INTO people (name) VALUES ('Steve Jobs');

7. Zsolt, has decided to hijack our movie evening, Boo! Remove him from the table of people.

  DELETE FROM people WHERE name = 'Zsolt Podoba-Szalai';

  DELETE 1

8. Somehow the list of people includes two people named 'instructor'. Change these entries to the proper names ('Darren Breen', 'Sandy McMillan')

10

UPDATE people SET name = 'Darren Breen' WHERE id IN (10);
UPDATE people SET name = 'Sandy McMillan' WHERE id IN (11);


9. The cinema has just heard that they will be holding an exclusive midnight showing of 'Guardians of the Galaxy 2'!! Create a new entry in the 'movies' table to reflect this.

INSERT INTO movies (title, year, show_time) VALUES ('Guardians of the Galaxy 2', 2017, '23:59');


10. The cinema would also like to make the Guardian movies a back to back feature. Update the 'Guardians of the Galaxy' show time from 12:10 to 21:30
 
 UPDATE movies SET show_time = '21:30' WHERE title = 'Guardians of the Galaxy';


## Extension

1. Research how to delete multiple entries from your table in a single command.
