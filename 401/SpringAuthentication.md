## Read: 16 - Spring Authentication


With Spring you can add security options, just like Auth0 back in 301. spring security help you add authentication and authorization to your web application.
  there are two main topics that Spring covers, in which are : 
 - authentication: to know how is the one that access the web application.
 - autherization: to know what is the role or access approvals he/ she has.
 
 
 **Authentication**
if you need your users to authenticate. That means your application will verify if the user is who he supposed to be, that will be done with a username and password.
by writing : 
``` java
public interface AuthenticationManager {

  Authentication authenticate(Authentication authentication)
    throws AuthenticationException;
}
```
you will be creating the auth method that you need, and this is how to add the password access :
``` java
@Configuration
public class ApplicationSecurity extends WebSecurityConfigurerAdapter {

  @Autowired
  DataSource dataSource;

   ... // web stuff here

  @Override
  public void configure(AuthenticationManagerBuilder builder) {
    builder.jdbcAuthentication().dataSource(dataSource).withUser("dave")
      .password("secret").roles("USER");
  }

}
```
authentication might be enough for simple web applications but if you want something more(with more features) 

read about   **Authorization**
if you want to determine whether this person is allowed to make some changes in a certain poing, this is what we call Authorization.
you need to give some of the users the access to the web normally, and you may need to add some more controle to yourself and other admins with you.


cheat sheet that was taken from :  /// https://github.com/codefellows/seattle-java-401d2/blob/master/SpringAuthCheatSheet.md?plain=1  ////
# Spring Auth Cheat Sheet

## Step 1: set up a user model and repo

## Step 2: create a controller for that model

## Step 3: UserDetailsServiceImpl implements UserDetailsService

gets a User from the database by username (make sure your repository has the method to make this easy!)

## Step 4: ApplicationUser implements UserDetails

use IntelliJ to implement the methods; make the boolean ones all return true

## Step 5: WebSecurityConfig extends WebSecurityConfigurerAdapter

- has a UserDetailsService
- passwordEncoder bean
- configure AuthManagerBuilder
    - `auth.userDetailsService(userDetailsService).passwordEncoder(passwordEncoder());`
- configure HttpSecurity
    - cors? csrf?
    - matchers for URLs that are allowed
        - ensure that login and signup URLs allowed; also consider homepage etc.
    - formLogin with login page set up
    - logout

```
    @Override
    @Bean
    public AuthenticationManager authenticationManagerBean() throws Exception {
        return super.authenticationManagerBean();
    }
```

## Step 6: registration page
- create it w/ form
- ensure it posts to a route your controller is ready for
- check it's saving in the DB
```
    // maybe autologin?
    Authentication authentication = new UsernamePasswordAuthenticationToken(newUser, null, new ArrayList<>());
    SecurityContextHolder.getContext().setAuthentication(authentication);
```

## Step 7: login page
- create it w/ form
- ensure it posts to the route you specified in web config
- try it out!
- add to a template w/ things about the Principal
