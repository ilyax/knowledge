# Git

I love Git and version control. And I use version control over any project I do. I follow a [series of rules](../../focusing/rules.md#git) when dealing with Git.

## Notes

- Commit as often as you can. Ideally after each micro-iteration, when something new is working.
  - This way, at the end of the day you can just rebase the whole branch and squash all of the micro-commits in a whole commit implementing the whole new features.
- Good git workflow to make changes to new projects: clone, fork (`hub fork`), 'git checkout -b my-feature', work, commit, 'git push -u nikitavoloboev my-feature', work, commit, 'git push'.
- If you’re doing things right, there’s only two kinds of branches anyways, master and feature branches. Feature branches can be squashed and rebased off master (minimizing the issue of merge conflicts and making for easier management of the commit history) and merged to master from there without requiring further conflict resolution. ([Trunk-Based Development](https://paulhammant.com/2013/04/05/what-is-trunk-based-development/))
- A Git branch is just a pointer to a commit. Git commits, however, also contain the hash of the parent commit(s), so by referring to that commit you also refer too all ancestors.
- Squash + rebase (for feature branches) are good for PRs. No one cares that it took you 20 tries to get the feature right, what matters is what went into the pull request, which is usually one commit.
- [To me the beauty of git stems from the fact that it is an implementation of a functional data structure. It‘s a tree index that is read-only, and updating it involves creating a complete copy of the tree and giving it a new name. Then the only challenge is to make that copy as cheap as possible - for which the tree lends itself, as only the nodes on the path to the root need to get updated. As a result, you get lock-free transactions (branches) and minimal overhead. It is so beautiful in fact that when I think about systems that need to maintain long-running state in concurrent environments, my first reaction is ”split up the state into files, and maintain it through git“.](https://news.ycombinator.com/item?id=21418033)
- [PRs with mandatory review within a company are a bit of an antipattern/red flag IMO. Cycle time automatically gets long. Even when pairing, changes can be put up for review if the authors want more feedback, so it's not a binary choice.](https://twitter.com/sanityinc/status/1313206571606978560)

## Links

- [Git from the Bottom Up (2008)](https://jwiegley.github.io/git-from-the-bottom-up/) ([HN](https://news.ycombinator.com/item?id=26884318))
- [Flight rules for git](https://github.com/k88hudson/git-flight-rules)
- [Great Git workflow instructions](https://github.com/rvolosatovs/turtlitto/blob/master/CONTRIBUTING.md)
- [GIT Conventions](https://medium.com/@tjholowaychuk/git-conventions-a940ee20862d)
- [Learn Git branching](https://learngitbranching.js.org/) ([Code](https://github.com/pcottle/learnGitBranching)) ([HN](https://news.ycombinator.com/item?id=24586436))
- [Gitbase](https://github.com/src-d/gitbase) - SQL interface to Git repositories.
- [Gitea](https://github.com/go-gitea/gitea) - Easiest, fastest, and most painless way of setting up a self-hosted Git service. ([Web](https://gitea.io/en-us/))
- [How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/)
- [How I Use Git](https://hugogiraudel.com/2018/02/17/how-i-use-git/)
- [clog-cli](https://github.com/clog-tool/clog-cli) - Generate beautiful changelogs from your Git commit history.
- [git rebase for fame and power](http://www.charlesetc.com/rebase-for-fame/)
- [gitbatch](https://github.com/isacikgoz/gitbatch) - Manage your git repositories in one place.
- [Conventional Commits](https://www.conventionalcommits.org/) - Specification for adding human and machine readable meaning to commit messages.
- [glint](https://github.com/brigand/glint) - Friendly tool for creating commits in the Conventional Commit style.
- [git absorb](https://github.com/tummychow/git-absorb) - Git commit --fixup, but automatic.
- [ghq](https://github.com/motemen/ghq) - Manage remote repository clones.
- [git-flow](https://github.com/nvie/gitflow) - Collection of Git extensions to provide high-level repository operations for Vincent Driessen's [branching model](http://nvie.com/git-model).
- [gitin](https://github.com/isacikgoz/gitin) - Commit/branch/status explorer for git.
- [Lab](https://github.com/zaquestion/lab) - Wraps Git or Hub, making it simple to clone, fork, and interact with repositories on GitLab.
- [Tips for a disciplined git workflow (2019)](https://drewdevault.com/2019/02/25/Using-git-with-discipline.html) ([Reddit](https://www.reddit.com/r/programming/comments/bfbar2/tips_for_a_disciplined_git_workflow/))
- [Git Town](https://github.com/Originate/git-town) - Generic, high-level Git workflow support.
- [libgit2](https://libgit2.org/) - Portable, pure C implementation of the Git core methods provided as a re-entrant linkable library.
- [git-delete-squashed](https://github.com/not-an-aardvark/git-delete-squashed) - Delete branches that have been squashed and merged into master.
- [rebase-editor](https://github.com/sjurba/rebase-editor) - Simple terminal based sequence editor for git interactive rebase.
- [git-standup](https://github.com/kamranahmedse/git-standup) - Recall what you did on the last working day. Psst! or be nosy and find what someone else in your team did.
- [git-rs](https://github.com/chrisdickinson/git-rs) - Implementing git in rust for fun and education.
- [Commit messages guide](https://github.com/RomuloOliveira/commit-messages-guide)
- [The Many Benefits of Using a Monorepo (2019)](https://pspdfkit.com/blog/2019/benefits-of-a-monorepo/) ([HN](https://news.ycombinator.com/item?id=19795482))
- [Lefthook](https://github.com/Arkweid/lefthook) - Git hooks manager.
- [git rebase in depth](https://git-rebase.io/) ([HN](https://news.ycombinator.com/item?id=19877811))
- [Highlights from Git 2.22 (2019)](https://github.blog/2019-06-07-highlights-from-git-2-22/)
- [What is a fork, really, and how GitHub changed its meaning (2019)](https://drewdevault.com/2019/05/24/What-is-a-fork.html) ([Lobsters](https://lobste.rs/s/txx8vu/what_is_fork_really_how_github_changed_its)) ([HN](https://news.ycombinator.com/item?id=20001570))
- [More productive Git](https://increment.com/open-source/more-productive-git/) ([HN](https://news.ycombinator.com/item?id=20004224))
- [List of commonly used Git commands](https://github.com/joshnh/Git-Commands)
- [Hercules](https://github.com/src-d/hercules) - Fast, insightful and highly customizable Git history analysis.
- [Git Tower Guides](https://www.git-tower.com/learn/)
- [git-stashout](https://github.com/aviaviavi/git-stashout) - Custom git checkout command to automatically manage a per-branch stash.
- [git-bug](https://github.com/MichaelMure/git-bug) - Distributed, offline-first bug tracker embedded in git.
- [Git Standards (2018)](https://blog.carlmjohnson.net/post/2018/git-gud/)
- [BFG Repo-Cleaner](https://github.com/rtyley/bfg-repo-cleaner) - Removes large or troublesome blobs like git-filter-branch does, but faster.
- [gitstatus](https://github.com/romkatv/gitstatus) - 10x faster implementation of `git status` command.
- [git-revise](https://github.com/mystor/git-revise) - Handy tool for doing efficient in-memory commit rebases & fixups.
- [git-secret](https://github.com/sobolevn/git-secret) - Bash-tool to store your private data inside a git repository.
- [pre-commit](https://github.com/pre-commit/pre-commit) - Framework for managing and maintaining multi-language pre-commit hooks.
- [git-o-matic](https://github.com/muesli/gitomatic) - Tool to monitor git repositories and automatically pull & push changes.
- [GitGraph.js](https://github.com/nicoespeon/gitgraph.js) - JavaScript library to draw pretty git graphs in the browser.
- [Git First-Parent-- Have your messy history and eat it too (2018)](http://www.davidchudzicki.com/posts/first-parent/)
- [Git Alias](https://github.com/GitAlias/gitalias) - Git alias commands for faster easier version control.
- [Git Interactive Rebase Tool](https://github.com/MitMaro/git-interactive-rebase-tool) - Native cross platform full feature terminal based sequence editor for git interactive rebase. Written in Rust using ncurses.
- [Apache Arrow Git Tips](https://andygrove.io/apache_arrow_git_tips/)
- [GitSheet](https://gitsheet.wtf/) - Dead simple git cheatsheet.
- [Git Commit naming](https://pbs.twimg.com/media/DBPQbTrXkAA4v-H.jpg)
- [HN: My Favourite Git Commit (2019)](https://news.ycombinator.com/item?id=21289827)
- [Onefetch](https://github.com/o2sh/onefetch) - Git repository summary on your terminal.
- [Delta](https://github.com/dandavison/delta) - Syntax-highlighting pager for git.
- [Building Git](https://shop.jcoglan.com/building-git/) - Deep dive into the internals of the Git version control system.
- [gitrs](https://github.com/haltode/gitrs) - Re-implementation of the git version control system in Rust.
- [sourcehut](https://sourcehut.org/) - Suite of open source tools for managing git projects. ([sr.ht](https://sr.ht/))
- [Sourcehut's year in alpha (2019)](https://sourcehut.org/blog/2019-11-15-sourcehut-1-year-alpha/) ([HN](https://news.ycombinator.com/item?id=21545145))
- [Sourcehut Project Hub](https://sourcehut.org/blog/2020-04-30-the-sourcehut-hub-is-live/) ([HN](https://news.ycombinator.com/item?id=23030489)) ([Lobsters](https://lobste.rs/s/y4zfxk/announcing_sourcehut_project_hub))
- [SourceHut's second year in alpha (2020)](https://sourcehut.org/blog/2020-11-15-sourcehut-2-year-alpha/) ([HN](https://news.ycombinator.com/item?id=25101359))
- [Awesome Monorepo](https://github.com/korfuri/awesome-monorepo) - Curated list of awesome Monorepo tools, software and architectures.
- [rug](https://github.com/samrat/rug) - Stripped-down version of Git, implemented in Rust.
- [Git from Beginner to Advanced](https://www.madebymike.com.au/writing/how-to-git/)
- [GitUp](https://gitup.co/) - Git client with nice interface. ([Code](https://github.com/git-up/GitUp))
- [Git from the inside out](https://codewords.recurse.com/issues/two/git-from-the-inside-out) ([HN](https://news.ycombinator.com/item?id=21755090))
- [Stacked Diffs Versus Pull Requests (2018)](https://jg.gg/2018/09/29/stacked-diffs-versus-pull-requests/)
- [Barebones git (2019)](https://artemix.org/blog/barebones-git.html) ([Lobsters](https://lobste.rs/s/7khgtp/barebones_git))
- [git-of-theseus](https://github.com/erikbern/git-of-theseus) - Analyze how a Git repo grows over time.
- [Git power tools for daily use (2018)](https://nvie.com/posts/git-power-tools/)
- [git-toolbelt](https://github.com/nvie/git-toolbelt) - Suite of useful Git commands that aid with scripting or every day command line usage.
- [git-series](https://github.com/git-series/git-series) - Track changes to a patch series over time.
- [Moving a Git Repository into Its Submodule (2020)](https://pspdfkit.com/blog/2020/moving-a-git-repository-into-its-submodule/)
- [Ignoring bulk change commits with git blame (2019)](https://www.moxio.com/blog/43/ignoring-bulk-change-commits-with-git-blame)
- [git-sizer](https://github.com/github/git-sizer) - Compute various size metrics for a Git repository, flagging those that might cause problems.
- [Release It](https://github.com/release-it/release-it) - Automate versioning and package publishing.
- [Git Magic](http://www-cs-students.stanford.edu/~blynn/gitmagic/) - Guide to using Git, a version control system. Fast, powerful, easy to learn.
- [git-crypt](https://github.com/AGWA/git-crypt) - Transparent file encryption in git.
- [Set up Keybase.io, GPG & Git to sign commits on GitHub](https://github.com/pstadler/keybase-gpg-github)
- [Bliss](https://github.com/ajmwagar/bliss) - "batteries included" .gitignore management tool.
- [Vaibhav Sagar - I Haskell a Git (2018)](https://www.youtube.com/watch?v=nVvvY5VRs8o)
- [Nx](https://github.com/nrwl/nx/) - Extensible Dev Tools for Monorepos.
- [Git Command Explorer](https://gitexplorer.com/) - Find the right commands you need without digging through the web. ([Code](https://github.com/summitech/gitexplorer))
- [Please stop recommending Git Flow (2020)](https://georgestocker.com/2020/03/04/please-stop-recommending-git-flow/) ([HN](https://news.ycombinator.com/item?id=22485489)) ([Lobsters](https://lobste.rs/s/o76cit/please_stop_recommending_git_flow))
- [git-trim](https://github.com/foriequal0/git-trim) - Automatically trims your tracking branches whose upstream branches are merged or gone.
- [A successful Git branching model (2020)](https://nvie.com/posts/a-successful-git-branching-model/)
- [Belay](https://github.com/JoshMcguigan/belay) - Makes it easy to run your CI checks locally, so you can git push with confidence.
- [Little Things I Like to Do with Git (2017)](https://csswizardry.com/2017/05/little-things-i-like-to-do-with-git/)
- [gsync](https://github.com/ScaleComputing/gsync) - rsync-like command to sync a git repo to a remote machine via git itself.
- [go-git](https://github.com/go-git/go-git) - Highly extensible Git implementation in pure Go.
- [Databases that use git as a backend? (2020)](https://lobste.rs/s/mb2hi2/databases_use_git_as_backend)
- [Self-hosting a tiny git remote (2020)](https://benjaminwil.info/weblog/self-hosted-git-remote/)
- [dgit](https://github.com/quorumcontrol/dgit) - Git with decentralized remotes. ([HN](https://news.ycombinator.com/item?id=22684945))
- [Setting Up Git Identities (2020)](https://www.micah.soy/posts/setting-up-git-identities/) ([HN](https://news.ycombinator.com/item?id=22672491))
- [Git Immersion](http://gitimmersion.com/) - Guided tour that walks through the fundamentals of Git, inspired by the premise that to know a thing is to do it.
- [Ship.js](https://github.com/algolia/shipjs) - Take control of what is going to be your next release.
- [Git Under the Hood Internals, Techniques, and Rewriting History (2019)](https://blog.isquaredsoftware.com/presentations/2019-03-git-internals-rewrite/#/)
- [libgit2](https://github.com/libgit2/libgit2) - Cross-platform, linkable library implementation of Git that you can use in your application.
- [lazygit](https://github.com/jesseduffield/lazygit) - Simple terminal UI for git commands.
- [My unorthodox, branchless git workflow (2020)](https://drewdevault.com/2020/04/05/My-weird-branchless-git-workflow.html) ([Lobsters](https://lobste.rs/s/lymznu/my_unorthodox_branchless_git_workflow)) ([HN](https://news.ycombinator.com/item?id=22793512))
- [Git Cola](https://git-cola.github.io/) - Sleek and powerful graphical user interface for Git. ([Code](https://github.com/git-cola/git-cola))
- [Ultra Runner](https://github.com/folke/ultra-runner) - Ultra fast monorepo script runner and build tool.
- [git-fame](https://github.com/casperdcl/git-fame) - Pretty-print git repository collaborators sorted by contributions.
- [Collection of .gitignore templates](https://github.com/github/gitignore)
- [CS Visualized: Useful Git Commands (2020)](https://dev.to/lydiahallie/cs-visualized-useful-git-commands-37p1)
- [git-issue](https://github.com/dspinellis/git-issue) - Git-based decentralized issue management.
- [git-filter-repo](https://github.com/newren/git-filter-repo) - Quickly rewrite git repository history (filter-branch replacement).
- [The Communicative Value of Using Git Well (2020)](https://jeremykun.com/2020/01/14/the-communicative-value-of-using-git-well/)
- [go-gitdiff](https://github.com/bluekeyes/go-gitdiff) - Go library for parsing and applying patches created by Git.
- [degit](https://github.com/Rich-Harris/degit) - Makes copies of git repositories.
- [Git branch naming conventions](https://deepsource.io/blog/git-branch-naming-conventions/) ([HN](https://news.ycombinator.com/item?id=23043881))
- [Git Command Overview with Useful Flags and Aliases (2020)](https://blog.jakuba.net/git-command-overview-with-useful-flags-and-aliases/)
- [Question: How does git detect renames? (2020)](https://chelseatroy.com/2020/04/20/question-how-does-git-detect-renames/) ([Lobsters](https://lobste.rs/s/bmfiiw/question_how_does_git_detect_renames))
- [Git Koans (2013)](https://stevelosh.com/blog/2013/04/git-koans/)
- [Sublime Merge](https://www.sublimemerge.com) - Git Client, done Sublime. Line-by-line Staging. Commit Editing. Unmatched Performance. ([[HN](https://news.ycombinator.com/item?id=23311093)])
- [GitUI](https://github.com/extrawurst/gitui) - Blazing fast terminal-ui for git written in rust.
- [gitea-release Tool Announcement (2020)](https://christine.website/blog/gitea-release-tool-2020-05-31)
- [git-fuzzy](https://github.com/bigH/git-fuzzy) - CLI interface to git that relies heavily on fzf. ([HN](https://news.ycombinator.com/item?id=23363767))
- [DeGit](https://github.com/yegor256/degit) - Decentralized Git projects hosting platform.
- [How to write good Git commit messages (2020)](https://altcampus.io/blog/how-to-write-good-git-commit-message) ([HN](https://news.ycombinator.com/item?id=23479465))
- [gitignore.io](https://www.toptal.com/developers/gitignore) - Create Useful .gitignore Files For Your Project. ([Code](https://github.com/toptal/gitignore.io))
- [Speeding up a Git monorepo at Dropbox with <200 lines of code (2020)](https://dropbox.tech/application/speeding-up-a-git-monorepo-at-dropbox-with--200-lines-of-code) ([HN](https://news.ycombinator.com/item?id=23480198))
- [Oh Shit, Git!?!](https://ohshitgit.com/) ([HN](https://news.ycombinator.com/item?id=24173238))
- [Using Rust to Delete Gitignored Cruft (2020)](https://www.forrestthewoods.com/blog/using-rust-to-delete-gitignored-cruft/)
- [The Problem with Git Flow (2020)](https://about.gitlab.com/blog/2020/03/05/what-is-gitlab-flow/) ([HN](https://news.ycombinator.com/item?id=23622071))
- [Ask HN: Git alternatives that aren't so complicated? (2020)](https://news.ycombinator.com/item?id=23670757)
- [Git Concepts I Wish I Knew Years Ago (2020)](https://dev.to/g_abud/advanced-git-reference-1o9j)
- [gitqlite](https://github.com/augmentable-dev/gitqlite) - Query git repositories with SQL. Uses SQLite virtual tables and go-git.
- [Git commit accepts several message flags (-m) to allow multiline commits](https://www.stefanjudis.com/today-i-learned/git-commit-accepts-several-message-flags-m-to-allow-multiline-commits/) ([HN](https://news.ycombinator.com/item?id=23767866))
- [A Better Way to Git Log to Understand Changes in a Big Codebase (2020)](https://pspdfkit.com/blog/2020/a-better-way-to-git-log/)
- [Write good commit messages (2020)](https://letterstoanewdeveloper.com/2020/07/27/write-good-commit-messages/) ([Lobsters](https://lobste.rs/s/z2vjet/write_good_commit_messages))
- [Just One Single History](https://github.com/esrlabs/josh) - Aimed at supporting trunk based development in a Git monorepo.
- [gix](https://github.com/Byron/gitoxide) - Idiomatic, modern, lean, fast, safe & pure rust implementation of git.
- [git-delete-merged-branches](https://github.com/hartwork/git-delete-merged-branches) - Convenient command-line tool helping you keep repositories clean. ([HN](https://news.ycombinator.com/item?id=24135860))
- [Using Askgit – A SQL interface to your Git repository (2020)](https://willschenk.com/articles/2020/using_askgit/) ([HN](https://news.ycombinator.com/item?id=24166489))
- [Trunk-based development (2020)](https://nelis.boucke.be/post/trunk-based-development/)
- [Good Commit Messages (2020)](https://lazau.com/articles/good_commit_messages.html) ([Lobsters](https://lobste.rs/s/0lwjby/good_commit_messages))
- [Ignoring mass reformatting commits with git blame](https://akrabat.com/ignoring-revisions-with-git-blame/)
- [cgit](https://git.zx2c4.com/cgit/about/) - Hyperfast web frontend for git repositories written in C.
- [Fork and Pull Request Workflow](https://github.com/susam/gitpr)
- [Git Internals - Learn by Building Your Own Git](https://www.leshenko.net/p/ugit/)
- [Stacked pull requests: Make code reviews faster, easier, and more effective](https://www.michaelagreiler.com/stacked-pull-requests/)
- [Create a global gitignore (2020)](https://mike.place/2020/global-gitignore/)
- [Fortunately, I don't squash my commits (2020)](https://blog.ploeh.dk/2020/10/05/fortunately-i-dont-squash-my-commits/) ([HN](https://news.ycombinator.com/item?id=24686527)) ([Reddit](https://www.reddit.com/r/coding/comments/j5l9wb/fortunately_i_dont_squash_my_commits/))
- [Git QuickFix](https://github.com/siedentop/git-quickfix) - Allows you to commit changes in your git repository to a new branch without leaving the current branch.
- [Gerrit is Awesome (2016)](https://techspot.zzzeek.org/2016/04/21/gerrit-is-awesome/)
- [Gerrit Code Review](https://www.gerritcodereview.com/)
- [Dulwich](https://github.com/dulwich/dulwich) - Pure-Python Git implementation. ([Web](https://www.dulwich.io/))
- [Ask HN: What are the pros / cons of using monorepos? (2020)](https://news.ycombinator.com/item?id=24719525)
- [bit](https://github.com/chriswalz/bit) - Modern Git CLI. ([HN](https://news.ycombinator.com/item?id=24751212)) ([Interview With Chris Walz of bit](https://chriswalz.com/posts/an-interview-with-chris-walz-of-bit/))
- [Copybara Action](https://github.com/olivr/copybara-action) - Transform and move code between repositories. Start with ZERO config and 100% customizable.
- [Git scraping: track changes over time by scraping to a Git repository (2020)](https://simonwillison.net/2020/Oct/9/git-scraping/) ([HN](https://news.ycombinator.com/item?id=24732943))
- [Branch Agnostic Git Aliases (2020)](https://aj.codes/post/branch-agnostic-git-aliases/) ([Lobsters](https://lobste.rs/s/z0spf3/branch_agnostic_git_aliases))
- [Beyond the Basics: 5 Powerful Advanced Tools in Git (2020)](https://codeburst.io/beyond-the-basics-5-powerful-advanced-tools-in-git-2180faf0ee29)
- [meta](https://github.com/mateodelnorte/meta) - Tool for managing multi-project systems and libraries. It answers the conundrum of choosing between a mono repo or many repos by saying "both", with a meta repo.
- [Self-hosting Git with cgit (2020)](https://peppe.rs/posts/self-hosting_git/) ([Lobsters](https://lobste.rs/s/mezxcr/self_hosting_git_with_cgit))
- [Embrace the monolith](https://www.monolithic.dev/) - Embrace a simpler way of building applications.
- [Better Git diff output for Ruby, Python, Elixir, Go and more (2020)](https://tekin.co.uk/2020/10/better-git-diff-output-for-ruby-python-elixir-and-more)
- [The Git Commit Hash (2020)](https://www.mikestreety.co.uk/blog/the-git-commit-hash)
- [git-secrets](https://github.com/awslabs/git-secrets) - Prevents you from committing secrets and credentials into git repositories.
- [Narrated Diffs](https://narrated-diffs.thomasbroadley.com/) - Tool to enable PR authors to tell a story with their changes. ([Code](https://github.com/tbroadley/narrated-diffs))
- [gitjacker](https://github.com/liamg/gitjacker) - Leak git repositories from misconfigured websites.
- [Git Magic](https://crypto.stanford.edu/~blynn/gitmagic/) - Guide to using Git. ([Code](https://github.com/blynn/gitmagic))
- [Git Crash Course (2020)](https://neros.dev/blog/git-crash-course-part-1/)
- [chglog](https://github.com/goreleaser/chglog) - Changelog management library and tool.
- [fzf powered git fixups (2017)](http://blog.railscoder.net/git/zsh/fzf/tmux/2017/10/24/fzf-powered-git-fixups.html)
- [Explain Git with D3](https://onlywei.github.io/explain-git-with-d3/) - Use D3 to visualize simple git branching operations. ([Code](https://github.com/onlywei/explain-git-with-d3)) ([HN](https://news.ycombinator.com/item?id=24957280))
- [My Thoughts On Monorepo (2020)](https://shekhargulati.com/2020/11/02/my-thoughts-on-monorepo/) ([HN](https://news.ycombinator.com/item?id=24971288))
- [Signed git pushes (2020)](https://people.kernel.org/monsieuricon/signed-git-pushes)
- [Towards an automated changelog workflow (2020)](https://blog.yossarian.net/2020/11/05/Towards-an-automated-changelog-workflow)
- [commit-autosuggestions](https://github.com/graykode/commit-autosuggestions) - Tool that AI automatically recommends commit messages.
- [GOMP](https://github.com/MarkForged/GOMP) - Tool for comparing branches.
- [This is how I git (2020)](https://daniel.haxx.se/blog/2020/11/09/this-is-how-i-git/) ([Lobsters](https://lobste.rs/s/0k1crw/this_is_how_i_git)) ([HN](https://news.ycombinator.com/item?id=25043731))
- [Trello Android's Git Branching Strategy (2020)](https://blog.danlew.net/2020/11/11/trello-androids-git-branching-strategy/)
- [Why Git blame sucks for understanding WTF code (and what you should use instead) (2020)](https://tekin.co.uk/2020/11/patterns-for-searching-git-revision-histories) ([Lobsters](https://lobste.rs/s/in8vp4/why_git_blame_sucks_for_understanding_wtf))
- [Git is simply too hard (2020)](https://changelog.com/posts/git-is-simply-too-hard) ([HN](https://news.ycombinator.com/item?id=25121416))
- [gfold](https://github.com/nickgerace/gfold) - CLI application that helps you keep track of multiple Git repositories.
- [git-ignore](https://github.com/janniks/git-ignore) - Interactive CLI to generate .gitignore files.
- [isomorphic-git](https://github.com/isomorphic-git/isomorphic-git) - Pure JavaScript implementation of git for node and browsers. ([Web](https://isomorphic-git.org/))
- [git-machete](https://github.com/VirtusLab/git-machete) - Makes merges/rebases/push/pulls hassle-free even when multiple branches are present in the repository.
- [Smithy](https://github.com/honza/smithy) - Tiny git forge written in Go.
- [Git Commands You Should Never Use (2020)](https://mquettan.medium.com/3-git-commands-you-should-never-use-99f6ec910989) ([HN](https://news.ycombinator.com/item?id=25217812))
- [Gitsight](https://www.gitsight.com/) - Derive insights from open source repositories and their contributors.
- [Gitopia](https://gitopia.org/#/) - Decentralized Source Code Collaboration Platform.
- [git wip: What the heck was I just doing? (2020)](https://carolynvanslyck.com/blog/2020/12/git-wip/) ([Lobsters](https://lobste.rs/s/mv8301/git_wip_what_heck_was_i_just_doing))
- [GitLab](https://gitlab.com/) - Open source end-to-end software development platform. ([Code](https://gitlab.com/gitlab-org/gitlab)) ([GitHub Mirror](https://github.com/gitlabhq/gitlabhq))
- [mob](https://github.com/remotemobprogramming/mob) - Tool for swift git handover. ([Web](https://mob.sh/))
- [uncommitted](https://github.com/brandon-rhodes/uncommitted) - Command-line tool to find projects whose changes have not been committed to version control.
- [Organise your commits (2020)](https://www.ncameron.org/blog/organise-your-commits/)
- [Experimenting with git storage (2020)](https://nedbatchelder.com//blog/202012/experimenting_with_git_storage.html) ([Lobsters](https://lobste.rs/s/pqlm33/experimenting_with_git_storage))
- [Fornalder](https://github.comn/hpjansson/fornalder) - Visualize long-term trends in collections of Git repositories.
- [What comes after Git? (2020)](https://twitter.com/jasoncwarner/status/1342172372061749248) ([HN](https://news.ycombinator.com/item?id=25535844))
- [Some of git internals](https://yurichev.com/news/20201220_git/)
- [Git email flow vs Github flow (2020)](https://blog.brixit.nl/git-email-flow-versus-github-flow/) ([Lobsters](https://lobste.rs/s/kevlgd/git_email_flow_vs_github_flow))
- [Git Commands to Live By (2020)](https://medium.com/better-programming/git-commands-to-live-by-349ab1fe3139) ([Reddit](https://www.reddit.com/r/programming/comments/kmxz65/git_commands_to_live_by_the_cheat_sheet_that_goes/))
- [git-chglog](https://github.com/git-chglog/git-chglog) - CHANGELOG generator implemented in Go.
- [GitRows](https://github.com/gitrows/gitrows) - Makes it easy to use and store data in GitHub and GitLab repos. ([Web](https://gitrows.com/))
- [How to keep your Git history clean with interactive rebase (2020)](https://about.gitlab.com/blog/2020/11/23/keep-git-history-clean-with-interactive-rebase/) ([Lobsters](https://lobste.rs/s/wp4ctv/how_keep_your_git_history_clean_with))
- [git-annex](https://git-annex.branchable.com/) - Allows managing files with git, without checking the file contents into git. ([Code](https://github.com/peti/git-annex))
- [gittup](http://gittup.org/gittup/) - Entire(-ish) linux distribution in git.
- [Git Extras](https://github.com/tj/git-extras) - GIT utilities -- repo summary, repl, changelog population, author commit percentages and more.
- [Gogs](https://github.com/gogs/gogs) - Painless self-hosted Git service. ([Web](https://gogs.io/))
- [git-big-picture](https://github.com/git-big-picture/git-big-picture) - Visualization tool for Git repositories.
- [Mango](https://github.com/axic/mango) - Git, completely decentralised. Using Ethereum and P2P content addressable networks (Swarm, IPFS, SSB) as a backend to Git.
- [git-url-parse](https://github.com/IonicaBizau/git-url-parse) - High level git url parser for common git providers.
- [pre-commit-hooks](https://github.com/pre-commit/pre-commit-hooks) - Some out-of-the-box hooks for pre-commit.
- [Cheatsheet to Rewrite Git History (2021)](https://blog.gitguardian.com/rewriting-git-history-cheatsheet/)
- [Why SQLite Does Not Use Git](https://sqlite.org/whynotgit.html)
- [A Visual Git Reference](http://marklodato.github.io/visual-git-guide/index-en.html)
- [Commitizen](https://github.com/commitizen-tools/commitizen) - Create committing rules for projects. Auto bump versions. Auto changelog generation.
- [simple-pre-commit](https://github.com/toplenboren/simple-pre-commit) - Simple pre commit hook for small open source projects.
- [git2go](https://github.com/libgit2/git2go) - Go bindings for libgit2.
- [Git Submodules: Adding, Using, Removing, Updating](https://chrisjean.com/git-submodules-adding-using-removing-and-updating/) ([HN](https://news.ycombinator.com/item?id=26164790))
- [Advanced Git Features You Didn’t Know You Needed (2021)](https://martinheinz.dev/blog/43) ([Lobsters](https://lobste.rs/s/bnsmni/advanced_git_features_you_didn_t_know_you))
- [Git Chain](https://github.com/Shopify/git-chain) - Tool to rebase multiple Git branches based on the previous one.
- [mit](https://github.com/mitchellwrosen/mit) - Git wrapper with a streamlined UX.
- [Git is my buddy: Effective Git as a solo developer (2021)](https://mikkel.ca/blog/git-is-my-buddy-effective-solo-developer/) ([HN](https://news.ycombinator.com/item?id=26239068))
- [git-gone](https://github.com/lunaryorn/git-gone) - Cleanup stale Git branches of pull requests.
- [Stacked Git](https://github.com/stacked-git/stgit) - Application for managing Git commits as a stack of patches. ([Web](https://stacked-git.github.io/))
- [git-notify](https://github.com/jevakallio/git-notify) - Communicate important updates to your team via git commit messages.
- [diff2html](https://github.com/rtfpessoa/diff2html) - Generates pretty HTML diffs from git diff or unified diff output. ([Web](https://diff2html.xyz/))
- [Oh My Git!](https://ohmygit.org/) - Open source game about learning Git. ([Code](https://github.com/git-learning-game/oh-my-git))
- [Improving large monorepo performance on GitHub (2021)](https://github.blog/2021-03-16-improving-large-monorepo-performance-on-github/) ([HN](https://news.ycombinator.com/item?id=26479127))
- [Self-Hosting Git (2020)](https://peppe.rs/posts/self-hosting_git/) ([HN](https://news.ycombinator.com/item?id=26490179))
- [Git scraping: tracking changes to a scraped data source using GitHub Actions (2021)](https://www.youtube.com/watch?v=2CjA-03yK8I) ([Tweet](https://twitter.com/simonw/status/1367632117127995393))
- [Git Plan](https://github.com/synek/git-plan) - Better workflow for git.
- [Those pesky pull request reviews (2021)](https://jessitron.com/2021/03/27/those-pesky-pull-request-reviews/) ([Tweet](https://twitter.com/jessitron/status/1376553051398488064))
- [On Git Commit Messages](https://github.com/michaeljones/on-commit-messages)
- [Commits are snapshots not diffs (2020)](https://github.blog/2020-12-17-commits-are-snapshots-not-diffs/) ([HN](https://news.ycombinator.com/item?id=26741829))
- [A look how branches work in Git (2021)](https://stackoverflow.blog/2021/04/05/a-look-under-the-hood-how-branches-work-in-git/) ([HN](https://news.ycombinator.com/item?id=26735628))
- [GitAhead](https://gitahead.github.io/gitahead.com/) - Graphical Git client for Windows, Linux and macOS. ([Code](https://github.com/gitahead/gitahead))
- [Gitlet.js](https://github.com/maryrosecook/gitlet) - Git implemented in JavaScript. ([Docs](http://gitlet.maryrosecook.com/docs/gitlet.html)) ([HN](https://news.ycombinator.com/item?id=26787376))
- [git-split-diffs](https://github.com/banga/git-split-diffs) - GitHub style split diffs with syntax highlighting in your terminal.
- [What’s wrong with Git? A conceptual design analysis (2016)](https://blog.acolyer.org/2016/10/24/whats-wrong-with-git-a-conceptual-design-analysis/) ([HN](https://news.ycombinator.com/item?id=26961044))
- [Scaling monorepo maintenance (2021)](https://github.blog/2021-04-29-scaling-monorepo-maintenance/) ([HN](https://news.ycombinator.com/item?id=26991505))
- [Clean Git House (2021)](https://write.rog.gr/dress-code/clean-git-house.html) - Guide about deleting branches in Git.
- [repostatus.org](https://www.repostatus.org/) - Standard to easily communicate to humans and machines the development/support and usability status of software repositories/projects. ([Code](https://github.com/jantman/repostatus.org))
- [Undercover](https://github.com/a7ul/undercover) - Store your environment variables and secrets in git safely.
- [gitgo](https://github.com/ChimeraCoder/gitgo) - Provides Go functions for interacting with Git repositories.
- [Convco](https://github.com/convco/convco) - Conventional commits, changelog, versioning, validation.
