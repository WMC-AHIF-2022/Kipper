# Development Use Case of Kipper

The primary use case and reason for the development of Kipper is the
simplification of the development process for developers, both in the web
and server-side space, by improving on common issues and helping developers
fix them more easily and quickly.

Therefore this programming language, like TypeScript, aims to provide more
safety and functionality using a compiler and pre-runtime error checking.
This primarily also utilises type checking, as a way to ensure that programs
work as intended and that developers can discover errors before they run their
code.

TypeScript already does a great job at this, so why is Kipper needed or how does
it do things differently? TypeScript is an amazing language, which is why Kipper
has many of its designs and features similarly implemented. Though a big issue
that TypeScript can't detect is and properly resolve is the issue of inconsistent
or incomplete typing. This is a huge issue when working with dynamic data or JavaScript
code, where types are unknown or can't be known before runtime, since due to the
compile time typing of TypeScript type checking often is not able to detect
issues and many will simply bypass error checks altogether. Even with
`instanceof` and `typeof` checks, it becomes a tedious effort that often results
in more errors, due to issues arising while trying to fix the original problems.

Kipper therefore tries to implement a way to easily solve those issues in a
standardised way, by allowing for more complex runtime type checks and runtime
error handling. This means Kipper will still be there to assist the developer
during runtime, by handling many cases where type issues could arise. This also
means functionality like casts or conversions are more strictly handled and don't
overwrite type checking behaviour. Even so though, Kipper will always try to not
be invasive, and developers can choose during development time how to handle
different cases and how Kipper should handle them during runtime.

# Specific Use Cases Kipper

## Web Development

Since Kipper compiles directly to either JavaScript or TypeScript, Kipper code
can be easily used within Browser environments and used to create web applications.
Support for Web APIs is also planned as a way to safely use standardised global
variables and classes.

## Node.js Server-side development

[Node.js Docs](https://nodejs.org/en/docs/)

Kipper may also be used for server-side applications using the standard Node.js
API. Here Kipper plans to also support natively the `@types/node` package, as a
way to stay up to date with the most recent Node.js versions and avoid the need
to maintain another type definition format.

## Deno Server-side development

[Deno Docs](https://deno.land/)

As Node.js is not the only runtime for JavaScript, Deno, which has been getting
more and more popular in the last few years, will also receive native support
and should be usable together with Kipper. Since Deno, does a few things differently
compared to Node.js, a specific Deno compile target will likely be provided as a
way to ensure compatibility is ensured.

## Bun Server-side development

[Bun Docs](https://bun.sh/)

Another runtime called Bun, which is still in development at the moment, will
also receive similar support like Deno, where a specific Bun compile target will
likely be provided.
