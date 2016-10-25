# Q0: Why is this error being thrown?

This error is being thrown because there is no Pokemon model yet.

# Q1: How are the random Pokemon appearing? What is the common factor between all the possible Pokemon that appear? *
    
The home_controller's index function generates Pokemon using a sample method. The generated Pokemon all do not belong to a trainer, so they may be captured.

# Question 2a: What does the following line do "<%= button_to "Throw a Pokeball!", capture_path(id: @pokemon), :class => "button medium", :method => :patch %>"? Be specific about what "capture_path(id: @pokemon)" is doing. If you're having trouble, look at the Help section in the README.

This creates a button on the page (displaying "Throw a pokeball!") that when clicked, invokes the capture function. Capture_path(id: @pokemon) takes in the ID of a captured Pokemon and specifies the path of the HTTP request to update the database models. Class specifies the HTML class of the element (for styling and javascript) and method specifies the patch verb used for updating a database.

# Question 3: What would you name your own Pokemon?

Bubbles

# Question 4: What did you pass into the redirect_to? If it is a path, what did that path need? If it is not a path, why is it okay not to have a path here?

trainer_path(id: @pokemon.trainer_id). Rails then formats the url with the appropriate id.

# Question 5: Explain how putting this line "flash[:error] = @pokemon.errors.full_messages.to_sentence" shows error messages on your form.

The line displays error messages at the top of the page by rendering the message method defined in application.html.erb. The message will be displayed by default on any rendered page, so this will alert the user upon invalid submission of the form.

# Give us feedback on the project and decal below!

Fun project, good amount of work.

# Extra credit: Link your Heroku deployed app
