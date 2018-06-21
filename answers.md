Album.where("artist_id =(?)",Artist.where("name = ?", "Queen").ids)

 mediatype  = MediaType.where("name = ?", "Protected MPEG-4 video file")

Track.where("media_type_id = (?)",mediatype[0].id).count

Genre.where("name =?", "Hip Hop/Rap")
genre  = Genre.where("name =?", "Hip Hop/Rap"
Track.where("genre_id = ?", genre.ids).count

Track.all.sum("milliseconds")


oudioformat = MediaType.where("name = ?", "MPEG audio file")
Track.where("media_type_id =?",oudioformat.id).order("unit_price").last

most = Track.where("media_type_id=?",oudioformat.id).order("unit_price").last
Most.name 

=> #<Track id: 6, album_id: 1, genre_id: 1, media_type_id: 1, name: "Put The Finger On You", composer: "Angus Young, Malcolm Young, Brian Johnson", milliseconds: 205662, bytes: 6713451, unit_price: 0.99e0, created_at: "2005-01-03 05:49:26", updated_at: "2014-01-29 22:14:56">

Artist.order("created_at").limit 2

genre  = Genre.find_by name: 'Electronica/Dance'
Track.where("genre_id =?", genre.id).order("unit_price").last



oudioformat = MediaType.where("name = ?", "MPEG audio file")
genre = Genre.where("name = ?", "Electronica/Dance")
Track.where("genre_id = ? and media_type_id = ?",genre.first.id,oudioformat.first.id)