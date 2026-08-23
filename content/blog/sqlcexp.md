+++
title = "The sqlc experience"
date = 2026-08-19
+++

In the start of my Go journey, I was still following some tutorials to understand how Go works aswell as how people structure their projects and common practices, while watching those tutorials one thing I noticed was the use of the Object Relational Mapping or ORMs especially Gorm, now I have nothing against ORMs but a part of me inside never really liked it for some reason. But I ignored it and just continued on and kept wondering why I could never like Go as a whole just because of this.
<br>
<br>
Then while I was working on <a href="https://github.com/haarshmap/bookie" class="button-link-accent">bookie</a>, one of my friends recommended me to use sqlc. At first I was kind of skeptical considering it was something that was completely new to me and I was not really the smartest when I was structuring my queries and the whole situation of not like ORMs as a whole. But I decided to use this opportunity to switch things up and actually try something know hoping it might help me understand the one thing that was making Go dull. 
<br>
<br>
Now before we move to sqlc I will talk about my dislike with ORMs first, which was the layer of abstraction between the SQL and the program, though it seemed simple I could not wrap my head around how to structure my queries with it and it just felt somewhat unnecessary to me. It felt like it was kind of overcomplicating and I was feeling kind of dumb which in turn made me slowly lose interest in Go aswell.
<br>
<br>
Now, to say that sqlc changed my whole perspective of Go is a huge understatement. So for starters unlike ORMs, sqlc is SQL first. What it means is you will be writing your own SQL queries and sqlc generates the queries in Go which then can be used in your program by calling the methods as usual. It is also type safe and the queries are sanitized.
<br>
<br>
But how does this work you may ask, we first start with making our sqlc.yaml file which will contain the locations of the files which contain the schema, queries and where our generated code will be kept. Here, we also mention which engine we use and which version.
<img src="/sqlcexp/theyamlfile.png"></img>

Now in the same location you can make your schema.sql which will essentially just contain your tables and its definitions and the query.sql file will contain the queries and after the files are created you can just use the sqlc generate command and if there's no errors you get yourself the code generated in Go. Now, if you want a more in depth example, you can check out the official <a href="https://docs.sqlc.dev/en/latest/" class="button-link-accent"> sqlc documentation. </a>
<br>
<br>
Now, the main reason why I liked using sqlc was the simple reason that I finally could understand how my program flow was going. So it wasn't just me half guessing with oh will this work but just being able to understand and make my queries for the specific need just felt too good. It's simplicity was truly what made me fall in love with it.
<br>
<br>
And using it to actually make my queries felt a lot more intuitive like, if I wanted A, I could just get A. It felt really simple and easy to use, especially for a beginner like me who was already struggling with that section of programming with Go.
<br>
<br>
Now am I against ORMs as whole? Not really, but it really is not something I would use again and would prefer using sqlc again. This was really just a small devlog which summarizes on what I really liked about sqlc and I hope you had fun reading through my experience of switching into sqlc from ORMs.