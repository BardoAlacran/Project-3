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

| Name            | Method | Endpoint                      | Description                                      | Body                                  | Redirects       |
| --------------- | ------ | ----------------------------- | ------------------------------------------------ | ------------------------------------- | --------------- |
| Home            | GET    | /                             | See the main page                                |                                       |                 |
| Log in form     | GET    | /login                        | See the form to log in                           |                                       |                 |
| Log in          | POST   | /login                        | Log in the user                                  | {mail, password}                      | /               |
| Sign Up form    | GET    | /signup                       | See the form to sign up                          |                                       |                 |
| Sign Up         | POST   | /signup                       | Sign up a user                                   | {mail, password}                      | /profile        |
| Log out         | GET   | /logout                        | Log out a user                                   |                                       | /               |
| Profile         | GET    | /profile                      | See the profile page with editable form          |                                       |                 |
| Profile edited  | POST   | /profile                      | Send user's data changed                         | {user_email, password                 | /profile}       |
| Collection      | GET    | /collection                   | See user's collection                     |                                       |                 |
| Game           | GET    | /collection/gameId               | Read game's information                         |                                       |                 |
| Game add form  | GET    | /collection/new                   | See form to upload a new game                  |                                       |                 |
| Game add       | POST   | /collection/new                   | Upload a game to user's collection             |                                       | /Collection/gameId |
| game edit form | GET    | /collection/gameId/edit          | See edit form with game's preloaded information |                                       |                 |
| game edit      | POST   | /userid/collection/gameId/edit   | Add game's new information                      |                                        | /collection/gameId |
| game delete    | POST   | /userid/collection/gameId/delete | Delete game from user's collection                 |                                       | /collection         |

## Models

Game model

```js
{
    Name: String,
    Year: String,
    Rating: String,
    Description: String,
    Number_of_players: String,
    Img: String,
    Playing_time: String,
    Difficulty: String,  
}
```
User model

```js
{
    Nickname: String,
    userEmail: String,
    hashedPassword: String,
    Age: Number,
}
```
