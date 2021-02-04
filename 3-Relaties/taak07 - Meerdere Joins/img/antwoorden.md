SELECT game.name, platform.platform, genre.genre FROM game LEFT JOIN platform ON game.platform_id = platform.id LEFT JOIN genre ON game.genre_id = genre.id WHERE game.name LIKE "b%"

SELECT game.name, platform.platform, genre.genre, game.year FROM game LEFT JOIN platform ON game.platform_id = platform.id LEFT JOIN genre ON game.genre_id = genre.id WHERE game.name and game.year = 2013
