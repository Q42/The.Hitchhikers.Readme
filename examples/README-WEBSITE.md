# Van Gogh Museum website

The repo contains the public website from the Van Gogh Museum in Amsterdam.
The website is made with dotnet's razor templates and enhanced with Vue on the front-end.

## ✨ See it in action ✨

| Environment  | Web | Cms |
| ------------ | ----| --- | 
| `prod`   | [Custom domain](https://www.vangoghmuseum.nl/) / [Azure websites](https://www.vangoghmuseum.nl/) | [View]() |
| `staging`| [View](https://www.vangoghmuseum.nl/) | 🚧 |
| `acc`    | [View](https://www.vangoghmuseum.nl/) | [View]() |
| `test`   | [View](https://www.vangoghmuseum.nl/) | [View]() |

## 🧰 External tooling

- [Jira for the backlog](https://www.atlassian.com/software/jira)
- [Azure DevOps for builds & releases](https://azure.microsoft.com)
- [Figma for the designs](https://figma.com)

## 🚀 Getting started

### Prerequisites
- [Visual Studio](https://visualstudio.microsoft.com/) or [Rider](https://www.jetbrains.com/rider/)
- [ASP.NET Core 6](https://dotnet.microsoft.com/en-us/download)
- [`COMPUTERNAME` as environment variable](../documentation/GUIDE-FOR-SOMETHING.md)
- Node Version Manager ([Mac](https://github.com/nvm-sh/nvm) | [Windows](https://github.com/coreybutler/nvm-windows))
- [SQL database with full-text indexes](../documentation/GUIDE-FOR-SOMETHING.md)

### Installation

- [Setup User Secrets](../documentation/GUIDE-FOR-SOMETHING.md)

### Development

The new website consists of the 3 (runnable) projects: `VanGogh.Web`, `VanGogh.IIIFServer`, and `VanGogh.Cms`. Please run Web/Cms over https, because not everything works without https.

- [Build or watch the Cms front-end](../documentation/GUIDE-FOR-SOMETHING.md)
- [Build or watch the Website front-end](../documentation/GUIDE-FOR-SOMETHING.md)
- Run the projects in your IDE
- Go to https://localhost:21001 for the website, go to https://localhost:21000 for the Cms and have fun!
### Deployment

Deploys to environments can be done in [Azure DevOps](https://azure.microsoft.com).
When doing a deploy to production, make sure to inform the product owner about potential downtime of the website/cms.

## 🤚 Good to know

- [Frontend concept](../documentation/GUIDE-FOR-SOMETHING.md)
- [Artobject images](../documentation/GUIDE-FOR-SOMETHING.md)

### Translations

All translated content is stored inside the project `VanGogh.Domain`'s `Resource/R.resx`
and `Resource/R.en.resx`. When entries are added to these files, Rider automatically generates
C# code. There is a unit test (look for `RTests`) that checks if translations exist in all languages.

### Migrations

To generate a migration, be sure to have the latest EF tools installed globally
(run `dotnet tool install -g dotnet-ef`), and then go into the folder
`VanGogh` and execute:

```
dotnet ef migrations add MIGRATIONNAME
```