# EnvHelper

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://raw.githubusercontent.com/manheim/env_helper/master/LICENSE)
[![Travis](https://img.shields.io/travis/manheim/env_helper.svg?maxAge=2592000&style=flat-square)](https://travis-ci.org/manheim/env_helper)
[![Hex.pm](https://img.shields.io/hexpm/v/env_helper.svg?maxAge=2592000&style=flat-square)](https://hex.pm/packages/env_helper)

Using system variables is good practice, and env helper helps you practice it.

## Installation

If [available in Hex](https://hex.pm/docs/publish), the package can be installed as:

  1. Add env_helper to your list of dependencies in `mix.exs`:

        def deps do
          [{:env_helper, "~> 0.0.1"}]
        end

## Usage

Create a module to keep your settings in, and then call the `system_env/2` macro with the name of the environment variable you want to use as a lowercase atom, and the value you want to be the default as a string. For example:

    defmodule Settings
      import EnvHelper
      system_env(:base_url, "localhost:9000")
    end

This maps the method `Settings.base_url` to the system environment variable `BASE_URL`, or to the default value if the environment variable is not set.


