fmdb


fmdb is a little tool to handle a database of film watched, or ToWatch
It requires bs4, sqlalchemy, and requests ; prettytables is optionnal

It records :
imdb_title_code | year release |  date_of_view | note you give | comments | date_of_insert_in_database | Seen or Unseen

and gets automagically on imdb the titles of the films, for a convenient search later.

you need to inform in your ~/.database_rc_file (adjust in fmdb this name) :

//
[fmdb]
url = sqlite:///path/to/sqlite_fmdb.sql   # or whatever sql db you'd like
browser = "xombrero -s movie"             # or whatever browser you'd like
//

add a film to database :
fmdb add -i tt1234567 [-t "your own title"] [-d YYYYmmdd] [-n x.x] [-c ""]
	-i : imdb code for movie
	-t : give a personnal title to the film if you want
	-d : date of watch
	-n : note, on a scale from 0 to 10
	-c : comments
	-S : seen
	-U : unseen   (default : film seen)

find a film in database :
fmdb find [-t title] [-i tt1234567] [-d YYYYmmdd] [-n x.x] [--note-sup-than x.x] [--note_inf_than x.x]
			[ --film-older-than YYYY ] [ --film-younger-than YYYY]
	
will print on your screen, and eventually open the imdb_entry on your browser.

author: Franck Labadille
