# Description
Presentation for Saint Thomas High School on the Scrum agile framework.

# Requirements

* [git](https://git-scm.com/)
* [hovercraft](https://github.com/regebro/hovercraft)
* [Python](https://www.python.org/) >= 3.5
* [Ruby](https://www.ruby-lang.org/en/) >= 2.6 with rake and bundler

For Fedora, you can meet the requirements by running:
```
sudo dnf install -y git ruby rubygem-{bundler,rake}
pip3 install --user hovercraft
```

# Install

```
git clone https://github.com/cvoltz/scrum.git
cd scrum
rake setup
```

# Build

```
rake build
```

# View

To open the browser to view the presentation, run:
```
rake view
```

# Modify

When working on the presentation, start `guard` by running:
```
rake guard
```

When the source files are changed, the presentation will automatically be
rebuilt. The browser page will need to be automatically reloaded.

# License

All files are released under the [GPL v3 license](LICENSE).
