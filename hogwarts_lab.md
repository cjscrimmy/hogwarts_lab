## Hogwarts lab

We've given you a starting point with all your models / sql / seeds pre-written (you lucky things!)

Don't forget to create your db, create the tables, seed your db!

### MVP:

- Add the RESTful routes for the students resource into the students controller

<table><thead>
<tr>
<th>HTTP VERB</th>
<th>ROUTE</th>
<th>Action</th>
<th>Used For</th>
</tr>
</thead><tbody>
<tr>
<td>GET</td>
<td>'/students'</td>
<td>index action</td>
<td>index page to display all students</td>
</tr>
<tr>
<td>GET &nbsp; &nbsp;</td>
<td>'/students/new' &nbsp; &nbsp; &nbsp;</td>
<td>new action &nbsp;</td>
<td>displays create student form   &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</td>
</tr>
  <tr>
<td>GET &nbsp; &nbsp;</td>
<td>'/students/:id'</td>
<td>show action &nbsp;</td>
<td>displays one student based on ID in the url</td>
</tr>
<tr>
<tr>
<td>POST</td>
<td>'/students' &nbsp;</td>
<td>create action</td>
<td>creates one student</td>
</tr>
<td>GET</td>
<td>'/students/:id/edit'</td>
<td>edit action</td>
<td>displays edit form based on ID in the url</td>
</tr>
<tr>
<td>POST</td>
<td>'/students/:id'</td>
<td>update action</td>
<td><em>replaces</em> an existing student based on ID in the url</td>
</tr>
<tr>
<td>POST</td>
<td>'/students/:id/delete'</td>
<td>destroy action</td>
<td>deletes one student based on ID in the url</td>
</tr>
</tbody></table>

- Add the corresponding views


### IMPORTANT Notes:

- In this start code we have two models (with corresponding db tables) Student and House (One House can have MANY students)
- We've included a hard-coded `select` in `new.erb` so you can specify the house when you create a student. Remember this is based on the relationship - a student references the `houses` table via `house_id`.
- You'll want to make this dynamic at some point - ie based on the actual database. Right now we're assuming that the four houses have ids 1-4. How can we get hold of the houses and make sure we use the right `house_id` in our form even if we've been deleting from our tables? (Meaning the ids might not start at 1)

- In our edit view we'll want to make our `select` reflect the current house of the student we are editing. You'll need to research how to set the state of a `select` - aka which `option` is currently selected. (you can also look at the pizza_shop solution)
