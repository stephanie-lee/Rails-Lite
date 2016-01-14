# Rails Lite

## Phase 1: Server Setup
The behind-the-scenes of what happens when you run "rails server". I used Rack, a middleware between the web server and web application framework, to start up the server.

## Phase 2: Basic Controller
Set up ControllerBase, which has the same functionality that ActionController::Base has in Rails. The ControllerBase has the methods to accept an HTTP request and fill out a response, most notably the `render` and `redirect_to` methods.

## Phase 3: Template Rendering
Evaluate ERB code with `Kernel#binding` and pass the result to `render`.

## Phase 4: Session Storing
Store session information in a cookie. The ControllerBase constructs a session from the first request and caches it so it can be returned in future calls to session.

## Phase 5: Routing and Params
Set up a `Route` object that knows what path to match, what controller it belongs to, and what method to run in that controller.
Set up a `Router` object that figures out which `Route` matches the requested path.
Parse query strings, using Regex, to captures params.
