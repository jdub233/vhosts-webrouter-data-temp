# vhosts-webrouter-data-temp
This is a temporary working repo for BU webrouter rules being generated from htaccess files.

The source htaccess files are from `/afs/.bu.edu/cwis/web/vhosts/`

I was able to extract 147 viable htaccess files that only contained redirect rules.

## Single redirects
From the set of 147, I extracted 127 that essentially contained a single host entry pointing to a single redirect target.

Single redirect rules are in the `vhosts-single-redirects/` directory.

### Non Path-preserving redirects 
Of the single redirects, 45 are rules that do not preserve the original path.  Non path preserving redirects are indicated with a `redirect_asis` directive in webrouter.

Non path-preserving redirects as webrouter rules are in `vhosts-single-redirects/asis-maps/`

### Path-preserving redirects

87 are rules that preserve the path of the original request.  Path preserving redirects are indicated with a `redirect` directive in webrouter

## Multiple redirects

The remaining 20 htaccess files contain multiple redirect targets for a single host entry.
