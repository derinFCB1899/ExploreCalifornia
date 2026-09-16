# Explore California

A historical ASP.NET Core MVC learning sample using a travel website to explore routing, Razor views, middleware, configuration, and form handling.

## What the code demonstrates

- A home controller and shared Razor layout.
- Attribute-based blog routes, including year and month constraints.
- A sample blog post rendered from a model.
- GET/POST controller actions and Razor form helpers.
- Configuration-driven developer exception pages and static file serving.

## Local setup

The project targets **.NET Core 2.2**. Reproducing this snapshot requires a compatible .NET Core 2.2 SDK/runtime environment, Git, and NuGet access. This framework is [out of support](https://dotnet.microsoft.com/en-us/platform/support/policy/dotnet-core); use the project for local historical study and upgrade its dependencies before further deployment.

From a terminal:

```sh
git clone https://github.com/derinFCB1899/ExploreCalifornia.git
cd ExploreCalifornia
dotnet restore ExploreCalifornia/ExploreCalifornia.csproj
dotnet run --project ExploreCalifornia/ExploreCalifornia.csproj --launch-profile ExploreCalifornia
```

The checked-in launch profile uses [http://localhost:5000](http://localhost:5000).

Useful routes:

| Route | Example |
| --- | --- |
| Home | `/` |
| Blog index | `/blog` |
| Sample post | `/blog/2024/3/example` |
| Form example | `/blog/create` |

## Repository structure

- `ExploreCalifornia/Controllers/`: home and blog actions.
- `ExploreCalifornia/Models/`: the `Post` model.
- `ExploreCalifornia/Views/`: Razor views and shared layout.
- `ExploreCalifornia/wwwroot/`: static travel pages, styles, fonts, and images.
- `ExploreCalifornia/Startup.cs`: services, middleware, and routes.

## Historical limitations

The blog post is hard-coded. The create action does not save posts, and the form example has no submit button. The application has no implemented authentication or database layer. An intentional middleware example throws an exception for paths containing `invalid`. No automated test project is included.

The run command and URL match the checked-in project and launch profile. A clean build and runtime session have not been revalidated for this documentation update.
