# neo4j-learning
Learning Neo4J one graph at a time

## Code
- CREATE (ee:Person { name: "Emil", from: "Sweden", klout: 99 })
- MATCH (ee:Person) WHERE ee.name = "Emil" RETURN ee;

- MATCH (ee:Person) WHERE ee.name = "Emil"
- CREATE (js:Person { name: "Johan", from: "Sweden", learn: "surfing" }),
- (ir:Person { name: "Ian", from: "England", title: "author" }),
- (rvb:Person { name: "Rik", from: "Belgium", pet: "Orval" }),
- (ally:Person { name: "Allison", from: "California", hobby: "surfing" }),
- (ee)-[:KNOWS {since: 2001}]->(js),(ee)-[:KNOWS {rating: 5}]->(ir),
- (js)-[:KNOWS]->(ir),(js)-[:KNOWS]->(rvb),
- (ir)-[:KNOWS]->(js),(ir)-[:KNOWS]->(ally),
- (rvb)-[:KNOWS]->(ally)

MATCH (ee:Person)-[:KNOWS]-(friends)
2
WHERE ee.name = "Emil" RETURN ee, friends