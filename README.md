# Titan OS TV Debug API — Developer Features and Hidden Menus

This repository documents my findings regarding a hidden developer-centric debugging API and undocumented features within Titan OS, a web-based operating system used on Philips, JVC, and other smart TVs.

Through independent research and testing, I’ve uncovered accessible URLs and Easter eggs that provide a rare look into the development process of Titan OS and how new features are staged and tested before public rollout.
🖥️ Discovery of the Debugging Interface (https://acc01.titanos.tv/)

I discovered that the URL https://acc01.titanos.tv/ is publicly accessible through any web browser, with no authentication or security restrictions.

This URL loads a live version of the Titan OS home screen interface, including banners, apps, and sections that are not yet available to consumers. The subdomain acc01 likely refers to “Access Control”, a common naming convention used for development or staging environments.
📨 Payload Mechanism — How Titan OS Communicates

From my observations, Titan OS appears to handle interactions through structured payloads (JSON objects) which manage system functions and feedback loops. This includes:

    Sending Payloads to the TV:
    Developers could send commands to the TV/emulator, such as:

        Launching apps

        Modifying UI elements

        Triggering specific system events

        Simulating remote control inputs

    Receiving Payloads from the TV:
    The system responds with diagnostic data, logs, application states, or performance metrics.

The fact that this API endpoint is openly accessible, combined with the dynamic content loaded from it, suggests that it was intended for internal developer testing only, but remains publicly exposed.
🎮 Konami Code Easter Egg — Unlocking Developer Menus

In addition to the debug interface, I discovered that inputting the Konami Code on the TV remote (Up, Up, Down, Down, Left, Right, Left, Right, OK, OK) unlocks a hidden menu related to “Freely”, a new free-to-air streaming service currently in development.

This indicates that Titan OS firmware contains developer/test modes, allowing developers to access pre-release features directly on production devices using hidden shortcuts.
🔍 Summary of Findings

    Titan OS exposes a developer debugging API via acc01.titanos.tv, which is publicly accessible.

    Payloads are used to manage system functions and retrieve diagnostic data, with no visible security or authentication.

    Hidden developer menus can be triggered via input sequences (Konami Code), revealing unreleased features such as “Freely”.

    These findings indicate that Titan OS has internal, undocumented developer tools baked into the system, likely used for staging new content and services.

⚠️ Disclaimer

This repository is for educational and research purposes only.
I do encourage or condone any misuse of this information.
