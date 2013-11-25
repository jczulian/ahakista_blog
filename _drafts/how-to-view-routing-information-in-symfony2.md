
To list all routes available in your application use
s router:debug

When you want to know more information about a specific route. Just take the route name you are interested in and

s router:debug my_route_name

You get then plenty of information about your route:

[router] Route "home"
Name         home
Pattern      /
Class        Symfony\Component\Routing\Route
Defaults     _controller: Symfony\Bundle\FrameworkBundle\Controller\RedirectController::redirectAction
             permanent: true
             route: sonata_admin_dashboard
Requirements 
Options      compiler_class: Symfony\Component\Routing\RouteCompiler
Regex        #^/$#s



