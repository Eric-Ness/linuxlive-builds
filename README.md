# linuxlive-builds

Where [linuxlive.com](https://linuxlive.com)'s **Build it for me** builds
distros. Each build is a branch, `build/<id>`, holding the spec and art made
in the Workshop, and a run of [build.yml](.github/workflows/build.yml) on that
branch: the same reusable
[linuxlive](https://github.com/Eric-Ness/linuxlive) build every distro uses,
which boots the ISO five ways, installs it to a disk and checks the result.

- Everything here is public: the branches, the runs and the ISOs, at
  `https://downloads.linuxlive.com/builds/<id>/`.
- Builds are kept for 30 days; [cleanup.yml](.github/workflows/cleanup.yml)
  then deletes the ISO, the Fedora image and the branch. A distro you want to
  keep belongs in your own GitHub, made from the
  [linuxlive-distro template](https://github.com/Eric-Ness/linuxlive-distro),
  and from there in the [Library](https://github.com/Eric-Ness/linuxlive-library).
- Distros with scripts or GitHub code of their own are not built here; the
  first job refuses them. Build those in your own GitHub.
- Only linuxlive.com starts builds, with its own token. Pull requests to this
  repository are not built.

Everything a build makes follows linuxlive.com's [rules](https://linuxlive.com/policy/).
Report a problem to abuse@linuxlive.com.

The workflows are under MIT No Attribution (see LICENSE); each distro's spec
and art belong to the person who made it.
