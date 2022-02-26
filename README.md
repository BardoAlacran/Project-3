# Project's name

"Curiosity's Starship- (CS)"

## Description
Cs is a post page starship where the user can add life tips to the rest of the net for everything, deppending on the level required for that tip (noob, mid, late, godlike).

## USER stories

**404** - The user can see a 404 page when a page does not exist.

**500** - the User can see an error page when there is a server problem.

**Index** - the User can access the homepage with login and signup

**Sign-up** - the User can sign up on the webpage.

**Log-in** - the User can log in on the webpage.

**Log-out** - the User can log out from the webpage.

**Profile** - the User can see the profile with favs, its own posts and edit them. Edit the profille remove post or the account.

**Posts** - The user can see the global posts.

**Select-theme** - the user can see the posts by a theme choosen, levels, etc.

**Add Post** - The user can add a Post by theme to the global collection.

**See Post** - The user can see It's post collection.

**Delete Post** - The user can delete it's post from the collection.

**Edit Post** - The user can Edit the it's post.

## BACKLOG

**Comments** - The user will be able to see and post comments to the post.

**See related posts** - Related posts per theme or tags at will.

## Routes

**Name**        **route**           **description**                                 **body**
  log In        get('/auth/login)   To log in on the page
  Sign up       post('/auth/signup) To sign up in on the page
  Posts         get('/')            main page of the website to see all posts
  Add Post      post('/add)         Add post with a form                            { img, level, theme, body}
  Edit Post     put('/post/:id)     Edit post with a form                           { img, level, theme, body}
  Detail post   get('/post/:id)     See post detail
  Delete post   delete('/post/id)   Delete a post
  Profile       get('/profile)      acces to the profile page                           

## Models

Post model

```js
{
    user: _id,
    date: date,
    isFav: boolean,
    body: String,
    level: String,
    Img: String, 
    theme: String
}
```
User model

```js
{
    name: String,
    userEmail: String,
    hashedPassword: String,
    Age: Number,
    img: String
}
```
