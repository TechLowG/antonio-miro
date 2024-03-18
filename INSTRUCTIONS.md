### Initial Setup

`npx create-next-app@14.0.4 antonio-nextauth5-clone`
```
√ Would you like to use TypeScript? Yes
√ Would you like to use ESLint? Yes
√ Would you like to use Tailwind CSS? Yes
√ Would you like to use `src/` directory? No
√ Would you like to use App Router? (recommended) Yes
√ Would you like to customize the default import alias (@/\*)? No
```
`cd folder`

`npx shadcn-ui@latest init`
```
√ Which style would you like to use? » New York
√ Which color would you like to use as base color? » Slate
√ Would you like to use CSS variables for colors? ... yes
```

`npx shadcn-ui@latest add button`

### Structure 

...

### Concex Clerk

convex setup: https://docs.convex.dev/quickstart/nextjs
``` 
npm i convex@1.8.0
npx convex dev - "a new project" - <enter>
[2]: npm run dev
convex.dev: login - open created project
.
clerk.com - login - create app: "antonio-miro-clone - 
```

clerk setup: https://clerk.com/ - login - add application
```
application name: antonio-miro-clone
create application
copy API KEYS to .env
.gitignore .env
npm i @clerk/nextjs@4.29.5
```

convex clerk tutorial: https://docs.convex.dev/auth/clerk
```
clerk dashboard - jwt templates - new template: "convex" - copy issuer field to convex/auth.config.js
npx convex dev  (validate is ready)
[2]: npm run dev
clerk dashboard - customization/branding - hide clerk branding: "on"
```

.env.local
```
CONVEX_DEPLOYMENT=

NEXT_PUBLIC_CONVEX_URL=

NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=
```

### Dashboard layout

...

### Sidebar

```
clerk dashboard: organizations - enable organizations
- jwt templates - convex - claims: add "org_role" & "org_id" - save changes
clerk dashboard: customizations - avatars - Default organization logo - initials - save changes
.
npx shadcn-ui@latest add dialog tooltip
localhost: login - create organization (+) - name: "test" - create org - skip
- create organization (+) - name: "two" - create org - skip
```

### Organisation sidebar

```
localhost: create new account - create an org - name: "invite-test" - invite first account, role: member
- email - accept invite - validate "invite-test" org is added
```

### Navbar

```
npx shadcn-ui@latest add input
npm i query-string@8.1.0 usehooks-ts@2.10.0
localhost: login as first account - remove "two" org - validate "invite members" not shown
```

### Deployment

foreach
```
git add .
git commit -m "XX: message"
git push
validate deployment succeed
```

once
```
github.com/new - create repo
use second option - "push an existing repo"
.
vercel.com/new - import - deploy
settings - environment variables - add from .env
```