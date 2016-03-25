# discogs2itunes

Update your iTunes album ratings with your Discogs ratings.

## Synopsis

This script will try to update the album rating value of your iTunes albuns by 
getting the rating of the same album on your Discogs colletion.

Differences in album titles and the usage of special characters on album names 
may prevent the script from recognising the albuns properly.

The script is available on both Ruby and Python. Both versions will perform the 
same tasks however, due to the way that both languages deal with character 
encoding, normalisation and parametrisation, the results may be different. 
Please use the one that produces the best results for your iTunes library.

Data files produced by the scripts are not interchangeable despite both of the 
scripts are using the respective marshal libraries.

## Getting Started

There are a couple of things needed for either of the scripts to work.

### Prerequisities

Follow the instructions for the version of the script that you wish to use.
Discogs instructions are required for both versions.

#### Discogs

A discogs user account is required (to obtain the ratings from). You can 
create an account at [https://www.discogs.com/users/create](https://www.discogs.com/users/create) 
if you do not have one already.

A discogs personal token is also required. You can obtain one at 
[https://www.discogs.com/settings/developers](https://www.discogs.com/settings/developers)


#### Ruby

For the Ruby version of the script the following gems are required:

* activesupport
* getoptlong
* httparty
* progress_bar
* rb-appscript

You can install gems with:

```
sudo gem install <gem_name>
```

Installing the httparty gem may require adicional options:

```
sudo gem install -n /usr/local/bin httparty
```

#### Python

For the Python version of the script the following modules are required:

* appscript
* getopt
* inflection
* json
* marshal
* os.path
* progress
* re
* requests
* sys
* time

You can install modules with:

```
sudo pip install <module_name>
```

The python script will also require openssl version 1.0. This script will not 
be able to connect to Discogs using TLS with the default openssl version on 
Mac OS X (which is 0.9.8).

### Installation

Nothing special to be done. Just download the version of the script that you 
wish to use.

### Usage

Both versions of the script use the same arguments.

#### Ruby

```
Usage:
  discogs2itunes.rb -u <username> -k <apikey> [-s -f <filename>]
Options:
  -h, --help       show help
  -k, --apikey     discogs api key
  -u, --username   discogs username
  -s, --songs      update itunes songs rating instead of album rating
  -f, --datafile   datafile name (optional)
```

#### Python

```
Usage:
  discogs2itunes.py -u <username> -k <apikey> [-s -f <filename>]
Options:
  --help, -h                   show help
  --apikey, -k <api_key>       discogs api key
  --username, -u <username>    discogs username
  --songs, -s                  update itunes songs rating instead of album rating
  --datafile, -f <filename>    datafile name (optional)
```

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

## Versioning

This project uses [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/fscm/discogs2itunes/tags). 

## Authors

* **Frederico Martins** - [fscm](https://github.com/fscm)

See also the list of [contributors](https://github.com/fscm/discogs2itunes/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
