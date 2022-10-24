External engine (alpha 2)
=========================

Using engines running outside of the browser for
[analysis on lichess.org](https://lichess.org/analysis).

Example provider
----------------

1. Create a token at https://lichess.org/account/oauth/token/create?scopes[]=engine:read&scopes[]=engine:write

2. Run:

   ```
   LICHESS_API_TOKEN=lip_*** python3 example-provider.py --engine /usr/bin/stockfish
   ```

3. Visit https://lichess.org/analysis

4. Open the hamburger menu and select the *Alpha 2* provider

Official provider
-----------------

An official (more user-friendly) provider is under development.

Will provide Stockfish 15 for 64-bit x86 platforms, built with profile-guided
optimization, automatically selecting the best available binary for your CPU.

Third party clients and providers
---------------------------------

> :wrench: :hammer: The protocol is subject to change.
> Please make an issue or [get in contact](https://discord.gg/lichess) to discuss.

Lichess provides an
[HTTP API for third-party clients and providers](https://lichess.org/api#tag/External-engine).
