# T3 Stack Explanation
- Thesis: This stack leverages the type safety advantages provided by typescript, ensuring that schemas are consistent across the full stack, from the database to the client-side code.

## Stack
- [NextJS](https://nextjs.org/) - Offloads client processing by preloading content in the server before serving the webpage
  - Wrapper around React JS framework with typescript
  - Fascilitates routing and api endpoint creation
- [TailwindCSS](https://tailwindcss.com/) - Enables CSS shorthand in layout code. Prioritizes convenience and code readability. This is not an opinionated component library. This is just a tool to write effective CSS quickly. ([Cheat Sheet Here](https://nerdcave.com/tailwind-cheat-sheet))
- [tRPC](https://trpc.io/) - Creates a typesafe api between the client and server. Amazing at validating request/response data via [Zod](https://zod.dev/).
- [Prisma](https://www.prisma.io/) - Type-safe database client and ORM. Declare your schema in your project repo. Your middleware and frontend can reference types defined in your schema. Can integrate with MongoDB, MySQL, PostgreSQL, and more.
- [NextAuth](https://next-auth.js.org/) (I'm not using this one) - NextJS authentication abstraction tool. Install the package, and forget about having to safely authenticate user sessions.

## Developer Tools
- [ESLint](https://eslint.org/) | [Typescript-ESLint](https://typescript-eslint.io/) - Highly specific, highly customizable linting rules to standardize code appearance and remove code smells.
- [Prettier](https://prettier.io/) - Very simple, opinionated code formatter to make Typescript pretty. This integrates well with ESLint.
- VSCode Extensions - Prettier (Runs prettier as a code formatter), ESLint (Recognizes ESLint configuration), Error Lens (Highlights ESLint warnings), TailwindCSS Intellisense (Displays syntax hints with tailwind class names)

## Bonus
[Here](https://www.youtube.com/watch?v=CQuTF-bkOgc)'s an interesting video explaining the problems with existing component libraries/styling tools. After working with Bootstrap and MUI, I agree with his assessment that those tools are nightmarish when you want to change a component's style or behavior, so I've started building our components from scratch. Many of them will become useful in future grit apps, so I'll abstract them to a "GRIT React Template" app if/when Seawraith is "finished".