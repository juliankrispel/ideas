# I want to write CLIs like this:

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
