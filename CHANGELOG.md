# Change Log

* 5.3.3
  * default webpackConfig.node should be false #502
  * Fix yarn list --json stdOut parsing. fixes #388 #516
  * Updated release notes #585
  * Updated Node versions in CI #587
  * Remove optional peer dependencies #542
  * Check for node runtimes first #579
  * Bumps lodash from 4.17.15 to 4.17.19 #602

* 5.3.2
  * Fix eslint prettier #518
  * Add TypeScript definition #520
  * Project dependencies updated #524
  * fix typescript example lockfile #526
  * Typescript example babel loader #527
  * Bump tar from 2.2.1 to 2.2.2 in /examples/babel #544
  * Bump acorn from 6.3.0 to 6.4.1 in /examples/typescript #562
  * Bump eslint-utils from 1.4.0 to 1.4.3 #567
  * Bump handlebars from 4.1.2 to 4.7.6 #568
  * Addressed npm security vulnerabilities #569
  * Bump https-proxy-agent from 2.2.2 to 2.2.4 #572
  * Bump https-proxy-agent from 2.2.2 to 2.2.4 in /examples/typescript #573
  * Bump extend from 3.0.1 to 3.0.2 in /examples/babel #574
  * Bump stringstream from 0.0.5 to 0.0.6 in /examples/babel #575
  * Bump tough-cookie from 2.3.2 to 2.3.4 in /examples/babel #576
  * Bump sshpk from 1.13.1 to 1.16.1 in /examples/babel #577
  * Bump debug from 2.6.8 to 2.6.9 in /examples/babel #578

* 5.3.1
  * Fixed bug that prevented to use handlers using import [#505][link-505]
  * Do not print empty lines in webpack stats [#499][link-499]
  * Added git hooks to improved code quality and developer experience [#496][link-496]

* 5.3.0
  * Restore compatibility with TypeScript [#449][link-449] [#465][link-465]
  * Allow glob for excludeFiles [#471][link-471]
  * Support Webpack 5 [#472][link-472]
  * Use colored output depending on tty [#480][link-480]
  * Allow to keep webpack folder [#453][link-453] [#467][link-467]
  * Add ability to exclude files from handler lookup [#433][link-433]
  * Documentation fixes [#429][link-429]

* 5.2.0
  * Show info message in verbose mode if aws-sdk has been excluded automatically [#393][link-393]
  * Added support for asynchronous webpack configuration [#412][link-412]
  * Better error message if handlers are not found [#418][link-418]

* 5.1.5
  * Re-publish of 5.1.4 without yarn.lock

* 5.1.4
  * Fix support for Yarn resolutions definitions [#379][link-379]
  * Better debugging for "Unable to import module ..." errors: Detect runtime dependencies that are only declared as devDependencies [#384][link-384]
  * Documentation updates [#382][link-382]

* 5.1.3
  * Fixed issue with Yarn and file references as dependencies [#370][link-370]

* 5.1.2
  * Fixed issue that leads to `Unexpected end of JSON` in projects with lots of dependencies [#309][link-309][#373][link-373]
  * Update webpack-4 example with VSCode debugging configuration [#365][link-365]

* 5.1.1
  * Fixed local invoke watch mode not executing changed files [#349][link-349]
  * Added Webpack 4 example [#355][link-355]
  * Documentation updates [#354][link-354]

* 5.1.0
  * Support Yarn [#286][link-286]
  * Allow local invoke to use existing compiled output [#341][link-341] [#275][link-275]
  * Support custom packager scripts [#343][link-343] [#342][link-342]

* 5.0.0
  * Support Webpack 4 [#331][link-331] [#328][link-328]
  * BREAKING: Drop support for Webpack 2
  * Allow to check for local invocation in the webpack configuration [#232][link-232]
  * New centralized configuration with fallback to the old one [#336][link-336]
  * Improved unit tests and actual coverage calculation [#337][link-337]

* 4.4.0
  * Support serverless-step-functions-offline [#313][link-313]
  * Fixed webpack documentation links [#326][link-326]
  * Abstracted packager interface [#329][link-329]

* 4.3.0
  * Add new `webpack:compile:watch:compile` event [#315][link-315]
  * Added note to README about using yarn [#316][link-316]
  * Made babel dynamic example the default babel example [#253][link-253]
  * Documentation fixes [#317][link-317] [#321][link-321]

* 4.2.0
  * Support local file references in package.json [#263][link-263]
  * Updated used tools (dev dependencies)

* 4.1.0
  * Prohibit manual entry configuration with individual packaging [#272][link-272]
  * Fixed bug with stats in webpack config for individual packaging [#278][link-278]
  * Fixed bug with startup order in combination with serverless-offline [#279][link-279]
  * Default target to "node" if not set [#276][link-276]
  * Support `serverless run` including watch mode [#269][link-269]

* 4.0.0
  * BREAKING: Expose lifecycle events for plugin authors [#254][link-254]
  * Fixed deprecated hook warning [#126][link-126]
  * Support forceExclude option for external modules [#247][link-247]
  * Support stats output configuration in webpack config [#260][link-260]
  * Google: Only integrate package.json but not node modules into artifact [#264][link-264]
  * Documentation fixes and updates [#265][link-265]
  * Updated examples [#250][link-250]

* 3.1.2
  * Fix issue where dependencies with dots in their names would not be installed [#251][link-251]

* 3.1.1
  * Fix issue where locked dependencies (package-lock.json) were ignored [#245][link-245]

* 3.1.0
  * Allow filesystem polling in watch mode (`--webpack-use-polling`) [#215][link-215]
  * Allow forced include of not referenced modules [#217][link-217]
  * Automatically include peer dependencies of used modules [#223][link-223]
  * Show explicit message if the provided webpack config can not be loaded [#234][link-234]
  * Improve examples [#227][link-227]
  * Update 3rd party provider compatibility table [#221][link-221]
  * Added automatic Travis and Coveralls builds to increase stability

* 3.0.0
  * Integrate with `serverless invoke local` [#151][link-151]
  * Support watch mode with `serverless invoke local --watch`
  * Stabilized and improved the bundling of node modules [#116][link-116], [#117][link-117]
  * Improved interoperability with Serverless and 3rd party plugins [#173][link-173]
  * Support individual packaging of the functions in a service [#120][link-120]
  * Allow setting stdio max buffers for NPM operations [#185][link-185]
  * Support bundling of node modules via node-externals whitelist [#186][link-186]
  * Removed the `webpack serve` command in favor of [`serverless-offline`][link-serverless-offline] [#152][link-152]
  * Updated examples [#179][link-179]
  * Added missing unit tests to improve code stability
  * Fixed unit tests to run on Windows [#145][link-145]

* 2.2.2
  * Reverted breaking change introduced in default output config [#202][link-202]

* 2.2.1
  * Restore functionality for Google provider [#193][link-193]

* 2.2.0
  * Allow full dynamic configurations [#158][link-158]
  * Fix a bug that prevented the entries lib export to work with TypeScript [#165][link-165]

* 2.1.0
  * Added support for webpack configuration in TypeScript format [#129][link-129]
  * Fixed bug with serverless-offline exec [#154][link-154]
  * Added unit tests for cleanup. Updated test framework [#11][link-11]
  * Support single function deploy and packaging [#107][link-107]
  * Fixed path exception bug with individual packaging and SLS 1.18 [#159][link-159]

* 2.0.0
  * Support arbitrary Webpack versions as peer dependency [#83][link-83]
  * Support `serverless offline start` invocation [#131][link-131]
  * Documentation updates [#88][link-88], [#132][link-132], [#140][link-140], [#141][link-141], [#144][link-144]
  * Print Webpack stats on recompile [#127][link-127]
