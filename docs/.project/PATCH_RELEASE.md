# Patch Release

__[Draft a patch release.](https://github.com/camunda/camunda-modeler/issues/new?body=%23%23%20What%27s%20inside%3F%0A%0A%3C%21--%20link%20changelog%20if%20available%20and%2For%20a%20version%20range%20%28i.e.%20%5B%60v4.9.0...develop%60%5D%28https%3A%2F%2Fgithub.com%2Fcamunda%2Fcamunda-modeler%2Fcompare%2Fv4.9.0...develop%29%29%20--%3E%0A%0A%2A%20...%0A%2A%20...%0A%2A%20...%0A%0A%0A%23%23%20Release%20Checklist%0A%0A_To%20be%20done%20immediately%20after%20creating%20this%20issue._%0A%0A%2A%20%5B%20%5D%20add%20Slack%20role%20to%20release%20manager%20%28%60%40modeling-release-manager%60%29%0A%0A_To%20be%20done%20to%20prepare%20and%20build%20the%20release._%0A%0A%2A%20%5B%20%5D%20make%20sure%20changes%20in%20upstream%20libraries%20are%20merged%20and%20released%0A%20%20%20%20%2A%20%60bpmn-js%60%2C%20%60dmn-js%60%2C%20%60%2A-properties-panel%60%2C%20%60%2A-moddle%60%2C%20%60camunda-bpmn-js%60%2C%20%60form-js%60%2C%20...%0A%2A%20%5B%20%5D%20make%20sure%20dependencies%20to%20upstream%20libraries%20are%20updated%20and%20can%20be%20installed%20%28%60rm%20-rf%20node_modules%20%26%26%20npm%20i%20%26%26%20npm%20run%20all%60%20works%29%0A%2A%20%5B%20%5D%20close%20all%20issues%20which%20are%20solved%20by%20dependency%20updates%0A%2A%20%5B%20%5D%20smoke%20test%20to%20verify%20all%20diagrams%20can%20be%20created%0A%2A%20%5B%20%5D%20update%20%5BRelease%20Info%5D%28https%3A%2F%2Fgithub.com%2Fcamunda%2Fcamunda-modeler%2Fblob%2Fmaster%2Fclient%2Fsrc%2Fplugins%2Fversion-info%2FReleaseInfo.js%29%0A%2A%20%5B%20%5D%20update%20%5B%60CHANGELOG%60%5D%28https%3A%2F%2Fgithub.com%2Fcamunda%2Fcamunda-modeler%2Fblob%2Fmaster%2FCHANGELOG.md%29%0A%2A%20%5B%20%5D%20create%20release%20%28%60npm%20run%20release%60%29%2C%20cf.%20%5Brelease%20schema%5D%28https%3A%2F%2Fgithub.com%2Fbpmn-io%2Finternal-docs%2Ftree%2Fmaster%2Frelease-schema%29%0A%20%20%20%20%2A%20%5B%20%5D%20wait%20for%20%5Brelease%20build%5D%28https%3A%2F%2Fgithub.com%2Fcamunda%2Fcamunda-modeler%2Factions%2Fworkflows%2FRELEASE.yml%29%20to%20create%20the%20%5Bartifacts%5D%28https%3A%2F%2Fgithub.com%2Fcamunda%2Fcamunda-modeler%2Freleases%29%0A%2A%20%5B%20%5D%20prepare%20a%20list%20of%20what%20was%20changed%20or%20needs%20to%20be%20tested%0A%2A%20%5B%20%5D%20execute%20integration%20test%2C%20verifying%20fixed%20things%20are%20actually%20fixed%0A%2A%20%5B%20%5D%20optionally%20trigger%20QA%20for%20testing%0A%0A_To%20be%20done%20to%20make%20the%20release%20publicly%20available._%0A%0A%2A%20%5B%20%5D%20publish%20release%20on%20%5BGithub%20Releases%5D%28https%3A%2F%2Fgithub.com%2Fcamunda%2Fcamunda-modeler%2Freleases%29%0A%2A%20%5B%20%5D%20trigger%20mirroring%20of%20release%20to%20%5BCamunda%20Download%20Center%5D%28https%3A%2F%2Fdownloads.camunda.cloud%2Frelease%2Fcamunda-modeler%2F%29%20via%20%5BJenkins%5D%28https%3A%2F%2Fci.cambpm.camunda.cloud%2Fjob%2Fsideprojects%2Fjob%2Fcamunda-modeler-desktop-RELEASE%2Fbuild%3Fdelay%3D0sec%29%0A%2A%20%5B%20%5D%20reach%20out%20to%20%60David%20Paradis%60%20so%20that%20he%20updates%20download%20version%20of%20%5BCamunda%20Modeler%5D%28https%3A%2F%2Fcamunda.com%2Fde%2Fdownload%2Fmodeler%2F%29%0A%2A%20%5B%20%5D%20add%20new%20version%20to%20%5Bupdate%20server%20releases%5D%28https%3A%2F%2Fgithub.com%2Fcamunda%2Fcamunda-modeler-update-server%2Fblob%2Fmaster%2Freleases.json%29%0A%2A%20%5B%20%5D%20publish%20release%20via%20update%20server%20%28push%20to%20%60live%60%29%0A&title=Release+Camunda+Modeler+vX.X.X&labels=release)__

## Template

A list of things to perform to cut a Camunda Modeler patch release.

```markdown
## What's inside?

<!-- link changelog if available and/or a version range (i.e. [`v4.9.0...develop`](https://github.com/camunda/camunda-modeler/compare/v4.9.0...develop)) -->

* ...
* ...
* ...


## Release Checklist

_To be done immediately after creating this issue._

* [ ] add Slack role to release manager (`@modeling-release-manager`)

_To be done to prepare and build the release._

* [ ] make sure changes in upstream libraries are merged and released
    * `bpmn-js`, `dmn-js`, `*-properties-panel`, `*-moddle`, `camunda-bpmn-js`, `form-js`, ...
* [ ] make sure dependencies to upstream libraries are updated and can be installed (`rm -rf node_modules && npm i && npm run all` works)
* [ ] close all issues which are solved by dependency updates
* [ ] smoke test to verify all diagrams can be created
* [ ] update [Release Info](https://github.com/camunda/camunda-modeler/blob/master/client/src/plugins/version-info/ReleaseInfo.js)
* [ ] update [`CHANGELOG`](https://github.com/camunda/camunda-modeler/blob/master/CHANGELOG.md)
* [ ] create release (`npm run release`), cf. [release schema](https://github.com/bpmn-io/internal-docs/tree/master/release-schema)
    * [ ] wait for [release build](https://github.com/camunda/camunda-modeler/actions/workflows/RELEASE.yml) to create the [artifacts](https://github.com/camunda/camunda-modeler/releases)
* [ ] prepare a list of what was changed or needs to be tested
* [ ] execute integration test, verifying fixed things are actually fixed
* [ ] optionally trigger QA for testing

_To be done to make the release publicly available._

* [ ] publish release on [Github Releases](https://github.com/camunda/camunda-modeler/releases)
* [ ] trigger mirroring of release to [Camunda Download Center](https://downloads.camunda.cloud/release/camunda-modeler/) via [Jenkins](https://ci.cambpm.camunda.cloud/job/sideprojects/job/camunda-modeler-desktop-RELEASE/build?delay=0sec)
* [ ] reach out to `David Paradis` so that he updates download version of [Camunda Modeler](https://camunda.com/de/download/modeler/)
* [ ] add new version to [update server releases](https://github.com/camunda/camunda-modeler-update-server/blob/master/releases.json)
* [ ] publish release via update server (push to `live`)
```

You may create a blank issue and copy the template into it.
