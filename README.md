# Alien::bison [![Build Status](https://secure.travis-ci.org/plicease/Alien-bison.png)](http://travis-ci.org/plicease/Alien-bison)

Find or build bison, the parser generator

# SYNOPSIS

From a Perl script

    use Alien::bison;
    use Env qw( @PATH );
    unshift @PATH, Alien::bison->bin_dir;  # bison is now in your path

From Alien::Base Build.PL

    use Alien:Base::ModuleBuild;
    my $builder = Module::Build->new(
      ...
      alien_bin_requires => [ 'Alien::bison' ],
      ...
    );
    $builder->create_build_script;

# DESCRIPTION

This package can be used by other CPAN modules that require bison,
the GNU Parser generator based on YACC.

# HELPERS

## bison

    %{bison}

Returns the name of the bison command.  Usually just `bison`.

# AUTHOR

Graham Ollis <plicease@cpan.org>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2017 by Graham Ollis.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
