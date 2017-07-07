# I want to write CLIs like this:

```
Eyo - Welcome to this {{green}}super amazing{{/green}} cli whoop whoop!
  So what do you want to do?
    c - create a new app -> ./create-new-app.sh
      Yippie!
      Your app is now created!
      You can run it by typing {{yellow}}npm start{{/yellow}}

    a - add a module to your app

      Where do you want your component? : component
        Which one?
          # Copies around files
          m - a middleware -> cp ./templates/middleware {{component}}
          r - a reducer -> cp ./templates/middleware {{component}}

    d - deploy the app -> ./deploy.sh
```

Possible applications:
- Scaffolding
- Text adventures
- Clis for environments - How often I wished there was a cli that just walked me through setting up a dev environment

## Here's a contrived example a cli tool that helps setting up a vm
```
Welcome to Project X, to cancel just press ctrl[c]
# To keep it simple, we could do if/else statements that rely on whether a process exits with 0 or 1

  if -> sudo service elasticsearch status
    {green}Elasticsearch running{/green}
  else
    Looks like elasticsearch isn't running, wanna restart it?
      - Yes -> sudo service elasticsearch restart
      - No

  if -> sudo service dynamo status
    - {green}Dynamo DB is running{/green}
  else
    Looks like dynamo isn't running, wanna restart it?
      - Yes
        if -> sudo service dynamo restart
          {green}Dynamo DB is running{/green}
        else
          I can't get dynamo db running sry dude, ask your sysadmin for help -> exit

      - No
```
