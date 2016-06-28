# sessionSix-Assignment1-


What are the movies that were released in 2012 and have >= 4.0 rating

val input = sc.textFile(“movies.txt”)

val mapInput = input.map(x => x.split(“,”))

val filterMap = mapInput.filter(x=> x(2).contains(“2012”))

val filteredMap = filterMap.filter(x=>x(3)  >= “4.0”)

filteredMap.collect()


List the movies per year

val input = sc.textFile(“movies.txt”)

val mapInput = input.map(x => x.split(“,”))

val mapByYear = mapInput.map(x  => (x,x(2)))

mapByYear.collect()



	
