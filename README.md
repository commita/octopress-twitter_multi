octopress-twitter_multi
=======================

Custom aside for Octopress to show multiple Twitter timelines

## Usage

* Clone repository to a temporary place

```bash
git clone https://github.com/commita/octopress-twitter_multi.git /tmp/octopress-twitter_multi
```

* Copy contents (except README.md) to the root of your blog

```bash
cp -r /tmp/octopress-twitter_multi/{source,sass} /path/to/blog
```

* *[optional]* Add the provided SASS partial to your custom styles file `sass/custom/styles.scss`

```scss
@import "twitter_multi.scss";
```

The provided style is meant to be used with the default Octopress theme (it's a
copy of the default Twitter aside actually). If you are not using the default
theme, then you can customize the timeline aside using the `.tweets` CSS class
(instead of the `#tweets` identifier).

* Configure Twitter accounts in `_config.yml`

```yaml
twitter_users:
  - username: first_tweeter
    tweet_count: 3
    show_replies: false
    follow_button: true
    show_follower_count: false
  - username: second_tweeter
    tweet_count: 3
    show_replies: false
    follow_button: true
    show_follower_count: false
```

* Add the aside to the `default_asides` list (or any other aside list you prefer) in `_config.yml`

```yaml
default_asides: [
  # asides/recent_posts.html, ...,
  custom/asides/twitter_multi.html
]
```

* Be happy and tweet about it
