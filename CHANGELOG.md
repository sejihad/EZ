# Changelog

## 1.0.0 (2026-04-28)


### Features

* add -q/--quiet flag to suppress warnings ([ef0c69c](https://github.com/sejihad/EZ/commit/ef0c69cacb415a038dce275289da0ca7499f72fb)), closes [#1396](https://github.com/sejihad/EZ/issues/1396)
* add c_string() builtin for C char* to EZ string conversion ([be5d313](https://github.com/sejihad/EZ/commit/be5d3137d433cad0f51845cc6a2ae86ab95f582d))
* **arrays:** add is_equal; reject array == / != with E3074 ([d31b01c](https://github.com/sejihad/EZ/commit/d31b01c2e4e75f78368e822a6230b1a802a44721))
* **binary:** implement all missing encode/decode functions ([#1334](https://github.com/sejihad/EZ/issues/1334)) ([c1642fc](https://github.com/sejihad/EZ/commit/c1642fc660140f414ba510aec98e5b0f61cbdb7f))
* **builtins:** add to_char() and char_count() for Unicode codepoint access ([#1512](https://github.com/sejihad/EZ/issues/1512)) ([80d00c0](https://github.com/sejihad/EZ/commit/80d00c040b9d8ef9a925c22632585ddbe87a751c))
* C interop via import c"header.h" and c.func() calls ([a26fcbe](https://github.com/sejihad/EZ/commit/a26fcbe7190aed6f21074d1d55a21c026f925b0b)), closes [#1398](https://github.com/sejihad/EZ/issues/1398)
* **c-interop:** add constant access, type validation, bigint rejection ([0e41d9a](https://github.com/sejihad/EZ/commit/0e41d9ad57b66ea5edc2fecaa388a1f0195786a9))
* **cli:** add --time and --no-color flags, hide --verbose ([641c0e3](https://github.com/sejihad/EZ/commit/641c0e3b1289fca7c660994a8255286fac224bfb))
* **cli:** expand ez report with cc, cpu, kernel, install path ([5740a5f](https://github.com/sejihad/EZ/commit/5740a5fb0be98f331bed91c74ba7591d775bc4da))
* **cli:** ez install &lt;version&gt; for pinned version install ([#1459](https://github.com/sejihad/EZ/issues/1459)) ([e10b6c3](https://github.com/sejihad/EZ/commit/e10b6c34d0dccb7b27bdc7c05039a09f7384db9a))
* **cli:** ez update --pre for pre-release installs ([#1460](https://github.com/sejihad/EZ/issues/1460)) ([22c6023](https://github.com/sejihad/EZ/commit/22c60231a92bbbe2d6c9dd9c10296e05991e5281))
* **cli:** version/report show both channels with structured labels ([5b9c8f5](https://github.com/sejihad/EZ/commit/5b9c8f5e906d4badb96c199ef75b95eb128346a6))
* **cli:** warn before replacing a dev build with a released binary ([d8771da](https://github.com/sejihad/EZ/commit/d8771dadd27586afa8f1e8c794511dee2247b974))
* **codegen, typechecker:** if/otherwise block scoping + null-check narrowing ([#1521](https://github.com/sejihad/EZ/issues/1521)) ([85b9d66](https://github.com/sejihad/EZ/commit/85b9d666f78e87471472441debf6622536cebcb8))
* **codegen, typechecker:** scope-based memory management — phase 2 + safety checks ([#1521](https://github.com/sejihad/EZ/issues/1521)) ([6e6509c](https://github.com/sejihad/EZ/commit/6e6509c1094fa8270f959470d7a13064754a55f3))
* **codegen:** monomorphise wildcard functions per call site ([#1443](https://github.com/sejihad/EZ/issues/1443) slice 3) ([79501dd](https://github.com/sejihad/EZ/commit/79501dd011c05cb95d59c87d145ed4c0949da1eb))
* **imports:** support extensionless file and directory imports ([1526cb6](https://github.com/sejihad/EZ/commit/1526cb6767548d1bc3c0da508d731848cf4a335f))
* **io:** add filesystem and path manipulation functions ([#1446](https://github.com/sejihad/EZ/issues/1446)) ([a788923](https://github.com/sejihad/EZ/commit/a788923e1031fdb14204c614ffc368845e114504))
* **maps:** add is_equal; reject map == / != with E3076 ([5d950eb](https://github.com/sejihad/EZ/commit/5d950ebf1645b4c2170bd45f498d0cd9d68b6516))
* module-qualified enums, transitive imports, import caching ([#1406](https://github.com/sejihad/EZ/issues/1406)) ([3b57169](https://github.com/sejihad/EZ/commit/3b57169cd9b03103e907dd2e8bcc8bce037428b5))
* **parser, codegen:** #json attribute for struct-based JSON ser/deser ([#1496](https://github.com/sejihad/EZ/issues/1496)) ([31decac](https://github.com/sejihad/EZ/commit/31decac0c22d3891f31676881180b5e52475fa36))
* **parser, typechecker, codegen:** wildcard struct fields ([#1520](https://github.com/sejihad/EZ/issues/1520)) ([f18ea37](https://github.com/sejihad/EZ/commit/f18ea375432328e6624c885f9ab4e4211ca8e1b5))
* **parser:** lex and parse wildcard type '?' in fn signatures ([#1443](https://github.com/sejihad/EZ/issues/1443) slice 1) ([0cbcb58](https://github.com/sejihad/EZ/commit/0cbcb582261344d1584f0fe2d09607b57d5756fb))
* **parser:** redirect IDENT IDENT at statement start to 'const' or 'mut' ([9cae303](https://github.com/sejihad/EZ/commit/9cae30348f7b6622b2623b85c4560b7b45305d1d))
* remove 'ez run' subcommand, ez &lt;file.ez&gt; is the only way ([5a6a37b](https://github.com/sejihad/EZ/commit/5a6a37b2edf058c511e15a5544380d4f4fce247c))
* **runtime, codegen:** scope-based memory management — phase 1 ([#1521](https://github.com/sejihad/EZ/issues/1521)) ([eecd021](https://github.com/sejihad/EZ/commit/eecd0216a5dddd9de70744adb6a72ceaf473d5bc))
* **stdlib:** add _result variants for all fallible stdlib functions ([#1547](https://github.com/sejihad/EZ/issues/1547)) ([9291e08](https://github.com/sejihad/EZ/commit/9291e083b45482f82667a7f54b281fd06d0c0266))
* **stdlib:** expand [@maps](https://github.com/maps) with size, merge, get_or_default, contains_value ([5460a82](https://github.com/sejihad/EZ/commit/5460a82b984577845b769592670286cdc841b9ab)), closes [#1333](https://github.com/sejihad/EZ/issues/1333)
* **stdlib:** io filesystem/path functions + uniform _result error handling ([c57d4b2](https://github.com/sejihad/EZ/commit/c57d4b2e4854a0cae734008ea56548544c0f34e6))
* **typechecker:** allow instance dispatch for struct functions; fix typed-func field calls ([1940954](https://github.com/sejihad/EZ/commit/19409547c1fb821678f806957e6d008ac94309a9))
* **typechecker:** emit W2012 on float when conditions ([40ce5ed](https://github.com/sejihad/EZ/commit/40ce5ed7b6e650119d44b4bb0eb1314304e893a2))
* **typechecker:** enforce #strict when exhaustiveness on enums ([acb166b](https://github.com/sejihad/EZ/commit/acb166ba0484dace9b5baa5221a7958398e1690b)), closes [#1424](https://github.com/sejihad/EZ/issues/1424)
* **typechecker:** implicit int-to-float coercion ([#1433](https://github.com/sejihad/EZ/issues/1433)) ([40ddbd1](https://github.com/sejihad/EZ/commit/40ddbd1b8ff9b4bbf404422e8c7bce5035b0c7ec))
* **typechecker:** instantiate wildcard functions at call sites ([#1443](https://github.com/sejihad/EZ/issues/1443) slice 2) ([3d216da](https://github.com/sejihad/EZ/commit/3d216da9cbebe42ee34873b22d82632c3cfe557f))
* **typechecker:** re-check generic bodies per instantiation ([#1443](https://github.com/sejihad/EZ/issues/1443) slice 4) ([6da2488](https://github.com/sejihad/EZ/commit/6da248819b6a2e7bdc428b1c304d4c6ee42d64cf))
* **typechecker:** reject 'return' inside main() with E3073 ([f8de701](https://github.com/sejihad/EZ/commit/f8de701e48839b8a8eaa090744abefc712baa08d))
* **types:** typed func — signatures end-to-end, bare func removed ([b94cf87](https://github.com/sejihad/EZ/commit/b94cf8746febb5411dc37e1f8b302c8f9740fe68))


### Bug Fixes

* 6 multi-file import codegen and type resolution bugs ([#1406](https://github.com/sejihad/EZ/issues/1406)) ([f588641](https://github.com/sejihad/EZ/commit/f588641deb457c83a8e1f1ce221f4fb5c6c37816))
* 7 multi-file import system bugs ([#1406](https://github.com/sejihad/EZ/issues/1406)) ([d41c2e1](https://github.com/sejihad/EZ/commit/d41c2e1e4301a33dd9077c3638aff3fdb07b5fcd))
* add missing import [@arrays](https://github.com/arrays) to nested_array_foreach test ([b852608](https://github.com/sejihad/EZ/commit/b85260891ef79147b3dd12a99a24b07922ecbc8a))
* add missing import [@arrays](https://github.com/arrays) to range_negative_step_for test ([2a9f155](https://github.com/sejihad/EZ/commit/2a9f1558d950e24e5141bd58c743a9bd43f1d9eb))
* **binary:** register all 48 functions in using-dispatch tables ([#1334](https://github.com/sejihad/EZ/issues/1334)) ([2b6a748](https://github.com/sejihad/EZ/commit/2b6a748836536214eb180176a16b35aca2c0b1a9))
* **c-interop:** error handling for missing imports, bad headers, EZ structs ([5d061df](https://github.com/sejihad/EZ/commit/5d061dfcd3dd6bf02ee295c9caadbb2169bbc965))
* **c-interop:** reserve 'c' module name to prevent collisions ([a848381](https://github.com/sejihad/EZ/commit/a848381d0dd6642e4e2977feb8608b2b7d68d1b7))
* **ci:** add error_codes to test link deps in ezc Makefile ([ff281c8](https://github.com/sejihad/EZ/commit/ff281c85954829fbb5ddb6697afbf2d1d6865775))
* **ci:** allow test steps to continue on failure and update e2e expectations ([a84bd88](https://github.com/sejihad/EZ/commit/a84bd88885500ed70421fbefc0d45ecb7035b305))
* **ci:** create embed stubs before go build in CI ([1d1e556](https://github.com/sejihad/EZ/commit/1d1e55666ef93e8ea2654ffa5951d7193f48c33c))
* circular import resolution and main file caching ([#1406](https://github.com/sejihad/EZ/issues/1406)) ([079c8c5](https://github.com/sejihad/EZ/commit/079c8c50e883ec9eed0d40b19169b3e562db4f94))
* **ci:** remove pz template type-check step ([4ed4769](https://github.com/sejihad/EZ/commit/4ed47690aa05430fbd1f6c3f9bb31450d65b1261))
* **ci:** run make stubs before staging embedded assets in release workflows ([2a8aad8](https://github.com/sejihad/EZ/commit/2a8aad889021a7fbb1e83300ed53c93e3153105f))
* **ci:** update beta-release workflow for single-binary build ([300a8a1](https://github.com/sejihad/EZ/commit/300a8a1d248f74656d550870b0dd35727e6fcc02))
* **cli:** add -q/--quiet flag to root command for direct file execution ([fb607f1](https://github.com/sejihad/EZ/commit/fb607f1d8c7c2387e027a00b6844ee4e1ef0cd1c))
* **cli:** allow ez update to install releases over dev builds ([1bdc2db](https://github.com/sejihad/EZ/commit/1bdc2db1d7967f41c37ec55dfccbd1832f59834e)), closes [#1550](https://github.com/sejihad/EZ/issues/1550)
* **cli:** clean up help output, remove redundant -v/--version and -h flags ([fe658b2](https://github.com/sejihad/EZ/commit/fe658b282634215d7c5077dc80f629bbd639295f))
* **cli:** error on unrecognized commands instead of silently showing help ([1fb26af](https://github.com/sejihad/EZ/commit/1fb26afe3cda1a5e90a39301d04bee363c5fae1d))
* **cli:** gate all Find() stat checks on regular-file mode ([#1461](https://github.com/sejihad/EZ/issues/1461)) ([a6c520e](https://github.com/sejihad/EZ/commit/a6c520e76c2d2cdffe90a37628a46e8bdf4a9b08))
* **cli:** skip ezc sibling directory in Find() fallback ([#1461](https://github.com/sejihad/EZ/issues/1461)) ([61b842b](https://github.com/sejihad/EZ/commit/61b842b68ce56a5b28874af88468b92890a7d12b))
* **cli:** validate file extensions and exit codes for check and pz ([b22dff3](https://github.com/sejihad/EZ/commit/b22dff31e1551d839a311ce7ec3bdad8c44ac29e))
* **codegen,parser:** quote strings/chars in composite prints; fix named returns with uppercase names ([7935421](https://github.com/sejihad/EZ/commit/7935421245e386a076b09b51de4cea37ba64c397))
* **codegen,runtime:** appending to zero-initialized struct array fields ([247920e](https://github.com/sejihad/EZ/commit/247920e5068ce413369e4466de7f59681ba35402))
* **codegen:** add crash guards for NULL arrays and snprintf overflow ([#1532](https://github.com/sejihad/EZ/issues/1532), [#1533](https://github.com/sejihad/EZ/issues/1533), [#1534](https://github.com/sejihad/EZ/issues/1534), [#1535](https://github.com/sejihad/EZ/issues/1535), [#1536](https://github.com/sejihad/EZ/issues/1536)) ([977f9ac](https://github.com/sejihad/EZ/commit/977f9ac1de391e480698eb4e1fd6e3f114a7a6dd))
* **codegen:** add ICE helper and fix unguarded typetable_get call ([#1524](https://github.com/sejihad/EZ/issues/1524)) ([9afc047](https://github.com/sejihad/EZ/commit/9afc047525632afdb084243e2d5c7534e78f45ac))
* **codegen:** add nil check for pointer field access ([#1528](https://github.com/sejihad/EZ/issues/1528)) ([893267a](https://github.com/sejihad/EZ/commit/893267a270643103412496c34e19646f25964aac))
* **codegen:** add overflow check to unary minus on signed ints ([7f73d08](https://github.com/sejihad/EZ/commit/7f73d086f0f05e8c77a6b376c95184dcf00e7e14))
* **codegen:** arrays module functions on pointer struct fields ([bcc5610](https://github.com/sejihad/EZ/commit/bcc5610f550716ffcd79a94d14a303bac2455f92))
* **codegen:** bind earlier params at call site so defaults can reference them ([6f90a9a](https://github.com/sejihad/EZ/commit/6f90a9a1825ccd2993d15974c971e5982daed98b))
* **codegen:** deep-copy arrays and strings assigned to struct fields inside if blocks ([4d6fda1](https://github.com/sejihad/EZ/commit/4d6fda1d49a7b39e7ff28c6b7fff88b47644dd91))
* **codegen:** deep-copy nested arrays in copy() and copy-on-assign ([#1465](https://github.com/sejihad/EZ/issues/1465)) ([fcf957a](https://github.com/sejihad/EZ/commit/fcf957aa2e6c226fc77fbd232e93ab6231d44a04))
* **codegen:** deep-copy struct array/map fields in copy() ([#1466](https://github.com/sejihad/EZ/issues/1466)) ([9b055bd](https://github.com/sejihad/EZ/commit/9b055bd08404991e8a38e9e466f215cb7650b458))
* **codegen:** defer file-scope array initialization to main() ([#1414](https://github.com/sejihad/EZ/issues/1414)) ([86cd019](https://github.com/sejihad/EZ/commit/86cd0192c44cf80c34e251705fb497007002471f))
* **codegen:** emit correct enum constant for rewritten cross-module enum access ([#1523](https://github.com/sejihad/EZ/issues/1523)) ([ae95285](https://github.com/sejihad/EZ/commit/ae95285313c8914903980fc767afdb4e420aa4c4))
* **codegen:** emit correct pointer type for for_each over [^T] arrays ([#1510](https://github.com/sejihad/EZ/issues/1510)) ([26d9250](https://github.com/sejihad/EZ/commit/26d9250ebda56c515dbf9cef1eb093ba33ba9fc9))
* **codegen:** emit void* for [func] array element storage ([#1439](https://github.com/sejihad/EZ/issues/1439)) ([9fee3f9](https://github.com/sejihad/EZ/commit/9fee3f99053a00538a08c1538da0dad6c2c5366d))
* **codegen:** emit void* for func refs in arrays.append and insert_at ([#1558](https://github.com/sejihad/EZ/issues/1558)) ([d4e0309](https://github.com/sejihad/EZ/commit/d4e0309fd3e9e3152f9c52dd9ea664606629c5c6))
* **codegen:** encode char as UTF-8 in string interpolation ([#1512](https://github.com/sejihad/EZ/issues/1512)) ([4ba1d22](https://github.com/sejihad/EZ/commit/4ba1d226da35588feb0d1c0d1111a54a38f21771))
* **codegen:** enum implicit values continue from last explicit value ([#1511](https://github.com/sejihad/EZ/issues/1511)) ([2cd34d0](https://github.com/sejihad/EZ/commit/2cd34d0e4b2224eadad88c9c532506ec25ae3968))
* **codegen:** escape newlines in raw string literals for valid C output ([36efb5c](https://github.com/sejihad/EZ/commit/36efb5cb69001d2d41eb1ebebe7bc861e77100aa)), closes [#1426](https://github.com/sejihad/EZ/issues/1426)
* **codegen:** float division by zero panics instead of producing inf ([ac8656a](https://github.com/sejihad/EZ/commit/ac8656a25666d3230322d70b5d121712eb370367)), closes [#1428](https://github.com/sejihad/EZ/issues/1428)
* **codegen:** fmt.pad_left/pad_right/center extract char from string arg ([f0fe08a](https://github.com/sejihad/EZ/commit/f0fe08a2f69ead2c111e374fa6e24650100394b0))
* **codegen:** fmt.sprintf was treating first arg as arena instead of format string ([283c700](https://github.com/sejihad/EZ/commit/283c7005cb4b4705232cff56146d80c26308c2dd))
* **codegen:** for_each + infix on wildcard params ([#1443](https://github.com/sejihad/EZ/issues/1443) follow-up) ([96906fc](https://github.com/sejihad/EZ/commit/96906fcfabf4aebdbaa6edf1208987061351e055))
* **codegen:** handle compound assignment on array-indexed sized types ([#1529](https://github.com/sejihad/EZ/issues/1529)) ([83ab361](https://github.com/sejihad/EZ/commit/83ab3615c82ed189dd4798ffa7346e1bd23ac544))
* **codegen:** handle pointer field assignment as lvalue with nil check ([#1531](https://github.com/sejihad/EZ/issues/1531)) ([0459ad0](https://github.com/sejihad/EZ/commit/0459ad0d1a19363ba83252f459fb3d5b0c486d65))
* **codegen:** hoist global constants before function definitions ([b7dfaf6](https://github.com/sejihad/EZ/commit/b7dfaf63d287262e633ff5d015254f71d50813b2))
* **codegen:** index-read, index-call, and assign on [func] arrays ([#1439](https://github.com/sejihad/EZ/issues/1439)) ([7be1a1a](https://github.com/sejihad/EZ/commit/7be1a1aa7598e540bc15fff14d973a8f662f1be4))
* **codegen:** initialize map and array fields in new() allocations ([643a352](https://github.com/sejihad/EZ/commit/643a3522cbdc8730ec5ffc00e16ad9eb6c42059e))
* **codegen:** json.encode() handles scalar types without address-of rvalue error ([bee0701](https://github.com/sejihad/EZ/commit/bee070133ead1fec54f0ba47398d51d269310a0f)), closes [#1307](https://github.com/sejihad/EZ/issues/1307)
* **codegen:** map key width for in/!in, has_key, remove_key ([#1430](https://github.com/sejihad/EZ/issues/1430)) ([d7c050d](https://github.com/sejihad/EZ/commit/d7c050d49cda9bc0bf269ba9e4a12408b10770f1))
* **codegen:** map ops on pointer struct fields no longer leak C errors ([313fd99](https://github.com/sejihad/EZ/commit/313fd99878ae21ce3c15c2aa93b4e57575dbded1))
* **codegen:** map variable with type annotation now uses initializer expression ([006fb0c](https://github.com/sejihad/EZ/commit/006fb0cbf05f677e7a5cb084e79f29f606627d1a)), closes [#1429](https://github.com/sejihad/EZ/issues/1429)
* **codegen:** overflow-check compound-assign on int and uint ([7c7f3c3](https://github.com/sejihad/EZ/commit/7c7f3c38f4bb940fe0d6e51cb2c35484cd2ded23))
* **codegen:** panic on signed int_min / -1 and int_min % -1 ([eaecf6a](https://github.com/sejihad/EZ/commit/eaecf6a121318c4ba24c426d7165d61bb77fce58))
* **codegen:** pointer arrays, pointer map values, bigint array indexing ([402d919](https://github.com/sejihad/EZ/commit/402d919e13873f4a7c99880943e9d397b0b0e8f0))
* **codegen:** prevent double-evaluation in sized-type compound assignment ([#1529](https://github.com/sejihad/EZ/issues/1529)) ([9830d41](https://github.com/sejihad/EZ/commit/9830d41824fb2dc32dfe6727043a74350d7f0951))
* **codegen:** print pointers as hex addresses, not auto-deref the pointee ([6db0462](https://github.com/sejihad/EZ/commit/6db0462c31f6fd6589f2ad49a6b8db644ae7d5b8))
* **codegen:** println/print on Error type prints the error message ([e259345](https://github.com/sejihad/EZ/commit/e2593459c7713b096611de5061960bf21aeda3f2)), closes [#1422](https://github.com/sejihad/EZ/issues/1422)
* **codegen:** register inferred-bigint vars so copy()/fn-return preserve i128/i256/u128/u256 ([46f3537](https://github.com/sejihad/EZ/commit/46f3537236b22231b8592cb0693b1d828c708d73))
* **codegen:** register ref() of struct field / array index as a transparent reference ([f7bde15](https://github.com/sejihad/EZ/commit/f7bde15e29555f50b6235efd787ffe02c7d05771))
* **codegen:** replace fixed 256-byte buffers with dynamic allocation ([#1537](https://github.com/sejihad/EZ/issues/1537), [#1538](https://github.com/sejihad/EZ/issues/1538)) ([3484928](https://github.com/sejihad/EZ/commit/34849284941842c7df8b72cce8a349bc468dd206))
* **codegen:** replace typeof() with concrete type and handle nested struct assignment ([#1529](https://github.com/sejihad/EZ/issues/1529), [#1544](https://github.com/sejihad/EZ/issues/1544)) ([ded0b7c](https://github.com/sejihad/EZ/commit/ded0b7ca002fbf6f405421d0755b0e1849f15778))
* **codegen:** resolve module-qualified names in member expressions ([fdc251e](https://github.com/sejihad/EZ/commit/fdc251e1a38cbd3ebe1bfbddb8a90d3d5ded57cb)), closes [#1419](https://github.com/sejihad/EZ/issues/1419)
* **codegen:** resolve module-qualified variables in for_each and all expressions ([064c39d](https://github.com/sejihad/EZ/commit/064c39d0d9f8961474c9cca7c0455567ff000b5c)), closes [#1419](https://github.com/sejihad/EZ/issues/1419)
* **codegen:** resolve unprefixed struct/enum names in type emissions ([ef71a35](https://github.com/sejihad/EZ/commit/ef71a35f872f17f49745c98df04f9bb62a1edd02))
* **codegen:** route nested-array var_decl copy-on-assign through deep copy ([#1465](https://github.com/sejihad/EZ/issues/1465)) ([e041dbe](https://github.com/sejihad/EZ/commit/e041dbe3c63029d570e144becd46276f8aca42b2))
* **codegen:** snapshot array length in for_each to prevent infinite loops ([bc77628](https://github.com/sejihad/EZ/commit/bc776289c93c1aca3b437524ba8fc814c29c1f7b))
* **codegen:** support bool/char/byte/float map keys ([#1430](https://github.com/sejihad/EZ/issues/1430)) ([af93fbf](https://github.com/sejihad/EZ/commit/af93fbf0ab2d2769f1642d7c254329caa06131b6))
* **codegen:** support element access on nested collection types ([#1464](https://github.com/sejihad/EZ/issues/1464)) ([8f5745d](https://github.com/sejihad/EZ/commit/8f5745d66f69d16eee34af3b67a77d54c4554158))
* **codegen:** support nested map types in literal emission ([#1464](https://github.com/sejihad/EZ/issues/1464)) ([658e641](https://github.com/sejihad/EZ/commit/658e641123c9901c83a7e26202e122f837db459c))
* **codegen:** suppress C unused-but-set-variable warning; deep-copy arrays on all assignments ([6aafa23](https://github.com/sejihad/EZ/commit/6aafa23588a49f8066f56817abb37a6bdd1c4f3f))
* **codegen:** unified deep-copy covering transitive/struct/map-of-struct gaps ([#1466](https://github.com/sejihad/EZ/issues/1466)) ([a366112](https://github.com/sejihad/EZ/commit/a366112416e495223984a4d960188e8b5daff603))
* **codegen:** use imported module list for member expression resolution ([1382ef8](https://github.com/sejihad/EZ/commit/1382ef8d125d67e014900b6ab54f907aa1d62685))
* **codegen:** use int64_t storage width for sized-type array compound assign ([#1529](https://github.com/sejihad/EZ/issues/1529)) ([9935901](https://github.com/sejihad/EZ/commit/9935901e1431d619a3d95355cc4e3a6cce4c01c7))
* **codegen:** use non-result io call for single-var assignments ([#1446](https://github.com/sejihad/EZ/issues/1446)) ([426bc32](https://github.com/sejihad/EZ/commit/426bc32af611ec8c6ef07133fc47b41504e25253))
* **codegen:** use typeof for sized-type compound assignment pointer ([#1529](https://github.com/sejihad/EZ/issues/1529)) ([ef25904](https://github.com/sejihad/EZ/commit/ef25904c1f5f09372a3aeb2859d87c7b61e4652f))
* **codegen:** value semantics for map and struct assignment ([ac3eba9](https://github.com/sejihad/EZ/commit/ac3eba941c22b363c317fa9dcd2939007f46de5c))
* **codegen:** wildcard multi-return uses base function name for EzMulti struct ([#1508](https://github.com/sejihad/EZ/issues/1508)) ([4206fb8](https://github.com/sejihad/EZ/commit/4206fb880ba5c09d0c379a409d93bab5e18fddb3))
* **codegen:** wrap string and char values in quotes inside composite prints ([39a4bfe](https://github.com/sejihad/EZ/commit/39a4bfe3ced0e17d80e59ea334b37fabc3dc25dc))
* **compiler:** resolve 4 failing integration tests ([#1521](https://github.com/sejihad/EZ/issues/1521)) ([6d64d55](https://github.com/sejihad/EZ/commit/6d64d55c7775ccb58e44fed982eab2c117a13a7b))
* complete import-and-use support for all 24 stdlib modules ([fbe0adb](https://github.com/sejihad/EZ/commit/fbe0adbc109d34ae990bdd5e51ae057aaac74b1c))
* derive EZ_VERSION from git tags at build time ([#1408](https://github.com/sejihad/EZ/issues/1408)) ([53513fc](https://github.com/sejihad/EZ/commit/53513fc47439ff28f46f2e157cc60bb8a8e4f27d))
* E2010 now checks source line ordering, not just existence ([19a9ce2](https://github.com/sejihad/EZ/commit/19a9ce2837e2ca5fc7a850d2f7148ffd6ffcfac3))
* **embed:** include runtime/stdlib source files in embedded binary ([8939aab](https://github.com/sejihad/EZ/commit/8939aab6102144506751337d12770990863123c0))
* empty map prints {:} instead of {} ([18825e1](https://github.com/sejihad/EZ/commit/18825e1f881ed7a258567ae6326f64227477a402)), closes [#1421](https://github.com/sejihad/EZ/issues/1421)
* enum-print test — use direct member assignment instead of int() cast ([30d071b](https://github.com/sejihad/EZ/commit/30d071bdc85a3a25dc4334ab359122bb0d339804))
* function-scoped using properly scoped, no leaking ([8759f13](https://github.com/sejihad/EZ/commit/8759f1330b72d82a113f341fc2c5325505d6daf8))
* helpful error for leading underscore in numeric literals ([#1407](https://github.com/sejihad/EZ/issues/1407)) ([44cadeb](https://github.com/sejihad/EZ/commit/44cadeb268c6783c57120ea6b0dcf15fbbeddbb9))
* import and use now exposes struct/enum types unqualified ([#1413](https://github.com/sejihad/EZ/issues/1413)) ([a01f58d](https://github.com/sejihad/EZ/commit/a01f58d4ba8ec13eef804512746e0fbd683787e5))
* **imports:** rewrite struct-namespaced func types and register aliases ([cf295f6](https://github.com/sejihad/EZ/commit/cf295f6c31cd80fdbb05147ec3a332088655c726))
* **imports:** rewrite struct/enum type names in var_decl and cast nodes ([7b85a90](https://github.com/sejihad/EZ/commit/7b85a90c3cab938f776dcdbd81bd12716371d9ac))
* **imports:** rewrite types in new(), nested func decls, and cast exprs ([db337a7](https://github.com/sejihad/EZ/commit/db337a7aaf5f2481105788811dba406ee23b3774))
* **io:** correct path_join, dirname, and extension edge cases ([#1446](https://github.com/sejihad/EZ/issues/1446)) ([84fc785](https://github.com/sejihad/EZ/commit/84fc785696f184ae3e8f47139b08866a7e793487))
* module collision detection — store path via arena_strdup ([#1406](https://github.com/sejihad/EZ/issues/1406)) ([7f884dc](https://github.com/sejihad/EZ/commit/7f884dc6ccd698557e2886967eee3629d8b69f82))
* multiple imports skipped due to stale si++ increment ([#1406](https://github.com/sejihad/EZ/issues/1406)) ([2086231](https://github.com/sejihad/EZ/commit/20862312cde860c6e3eff94f73ddf55a83c29014))
* **parser, codegen:** wildcard named returns -&gt; (name ?) ([#1502](https://github.com/sejihad/EZ/issues/1502)) ([796f992](https://github.com/sejihad/EZ/commit/796f992a20ee78e51ac9da4fdd066b7d3c108b8c))
* **parser,codegen:** remove E2077 whitespace restriction on struct literals; support json.parse() into arrays of #json structs ([a41e917](https://github.com/sejihad/EZ/commit/a41e917b85ea693c5a3486d297a663c047b46f37))
* **parser,codegen:** support ^^T pointer-to-pointer types ([#1504](https://github.com/sejihad/EZ/issues/1504)) ([86c2586](https://github.com/sejihad/EZ/commit/86c2586b5b73f70e04b704d727092bbfde22cfc9))
* **parser,typechecker:** catch 'nil' used as a variable type ([aee1770](https://github.com/sejihad/EZ/commit/aee1770c6f3e45b837f4b380197f9915502a4f75))
* **parser:** accept pointer types inside array and map type annotations ([e41e72a](https://github.com/sejihad/EZ/commit/e41e72a24d82eb880a6b754623053bba7ae1f763)), closes [#1442](https://github.com/sejihad/EZ/issues/1442)
* **parser:** add error recovery to prevent cascading parse errors ([7967500](https://github.com/sejihad/EZ/commit/79675001975cb3035e02b51d6b71c2c588c7c153)), closes [#1366](https://github.com/sejihad/EZ/issues/1366)
* **parser:** add missing when/ensure cases to import label rewriting ([#1523](https://github.com/sejihad/EZ/issues/1523)) ([cfd93e5](https://github.com/sejihad/EZ/commit/cfd93e560fcc80303f98072e90e570dffe28e9d8))
* **parser:** backfill type for comma-grouped struct fields ([#1495](https://github.com/sejihad/EZ/issues/1495)) ([e4fea14](https://github.com/sejihad/EZ/commit/e4fea146db06c52169bcef32ce678b49dfeeaea5))
* **parser:** emit E2017 for leading commas in array/map literals ([2ff10e8](https://github.com/sejihad/EZ/commit/2ff10e8aa80652b43c6bf521bc680dcdfdc354b0))
* **parser:** error on `name &type` parameter form instead of hanging ([79734f6](https://github.com/sejihad/EZ/commit/79734f6ccc3f8af389e5f62f3058b66f1fa72c6a))
* **parser:** for_each on uppercase-named constants no longer parsed as struct literal ([#1411](https://github.com/sejihad/EZ/issues/1411)) ([a869f52](https://github.com/sejihad/EZ/commit/a869f52afb016da3912fdd7f56744dba82260d60))
* **parser:** for_each with module-qualified collection no longer misparses ([#1415](https://github.com/sejihad/EZ/issues/1415)) ([2fd1e67](https://github.com/sejihad/EZ/commit/2fd1e67c079c4805425a6635c92331ebe6ab1f6f))
* **parser:** named return variables with pointer/array/optional types ([cdd96bc](https://github.com/sejihad/EZ/commit/cdd96bc37ea07ee1cfca1ae235cc7017e6d1e14f))
* **parser:** prevent struct literal parsing on RHS of in/not_in ([2644d3c](https://github.com/sejihad/EZ/commit/2644d3c705bede7494ba8af057194caec772bb63))
* **parser:** reject '&' as unary address-of operator ([#1547](https://github.com/sejihad/EZ/issues/1547)) ([e5148e1](https://github.com/sejihad/EZ/commit/e5148e147934bed9b268d4f1b28d7f6826a5dd30))
* **parser:** reject empty string interpolation '\${}' with targeted E2071 ([#1484](https://github.com/sejihad/EZ/issues/1484)) ([0a068f9](https://github.com/sejihad/EZ/commit/0a068f96b57cf79cedfd3722d6f4ed55cbe289ac))
* **parser:** reject semicolons in struct/enum declarations with E2069 ([26e80b1](https://github.com/sejihad/EZ/commit/26e80b1e0b1aba6e76bf39e11d8c40c05912ebe8)), closes [#1410](https://github.com/sejihad/EZ/issues/1410)
* **parser:** reject whitespace between function name and '(' in calls ([f6309e4](https://github.com/sejihad/EZ/commit/f6309e4bb6f9da0b7bd5ee661003b337cf1ce71f))
* **parser:** reject whitespace in member, index, postfix, and struct-literal syntax ([4433da5](https://github.com/sejihad/EZ/commit/4433da5daf1781dd42a111322b3a19b0db8ab16a))
* **parser:** reject wildcard '?' in enum variant and struct field name slots ([#1481](https://github.com/sejihad/EZ/issues/1481) follow-up) ([9d175d9](https://github.com/sejihad/EZ/commit/9d175d9789c529d6d817764456be9a6c509fc1ea))
* **parser:** route bare wildcard '?' in var_decl through E2070 ([#1481](https://github.com/sejihad/EZ/issues/1481)) ([01a7727](https://github.com/sejihad/EZ/commit/01a7727e579c82b18ea714a5d524f7869f8a22c0))
* **parser:** skip #doc attribute on struct functions ([#1518](https://github.com/sejihad/EZ/issues/1518)) ([c897eb7](https://github.com/sejihad/EZ/commit/c897eb7a302396219f6099481c17d1973e8ec7ed))
* **parser:** support map[...] nested inside collection type annotations ([#1464](https://github.com/sejihad/EZ/issues/1464)) ([969c332](https://github.com/sejihad/EZ/commit/969c3328edd61d3db7bb8d47268e0bc052221c0c))
* pointer types in array/map annotations and bigint array codegen ([c4528a1](https://github.com/sejihad/EZ/commit/c4528a1e267edc100bc15c4df763e8eb801fcbf8))
* qualified type annotations and type resolution for imports ([#1406](https://github.com/sejihad/EZ/issues/1406)) ([875cbfc](https://github.com/sejihad/EZ/commit/875cbfcf0eadb37b11e70a9a2ff95443a1933009))
* reject inline struct/enum declarations and semicolons ([#1410](https://github.com/sejihad/EZ/issues/1410)) ([576911e](https://github.com/sejihad/EZ/commit/576911e96d74962376af53a0760669cff282d8f3))
* reject using without import and unimported module access ([3bc8d25](https://github.com/sejihad/EZ/commit/3bc8d259cc9ee834d039aeee54f9bd0cbba7e429))
* remove broken top-level make test target ([#1521](https://github.com/sejihad/EZ/issues/1521)) ([6f6bc79](https://github.com/sejihad/EZ/commit/6f6bc793a32639d159dcc3d00f50527a2157f06d))
* remove dead code, fix standard inconsistencies ([#1334](https://github.com/sejihad/EZ/issues/1334)) ([64b7bc5](https://github.com/sejihad/EZ/commit/64b7bc544f6970cc75228e90f1d3aa823867aa3b))
* rename c.ez to deepmod.ez in transitive import test ([8b914df](https://github.com/sejihad/EZ/commit/8b914df5a02dd10300b11ba53cb7f31a83eaa98b))
* rename stdlib ez_atomic.h to ez_atomic_mod.h to resolve header collision ([37c7e4a](https://github.com/sejihad/EZ/commit/37c7e4abd81f3deb0da8f72335aae211555c6bac)), closes [#1425](https://github.com/sejihad/EZ/issues/1425)
* **repl:** output accumulation, path leaks, and noisy warnings ([1e43f54](https://github.com/sejihad/EZ/commit/1e43f548db71f86ba0542709b2303d885025401d)), closes [#1420](https://github.com/sejihad/EZ/issues/1420)
* resolve 4 multi-file import bugs ([131b068](https://github.com/sejihad/EZ/commit/131b068aebbb4456b9029d67ed5ba96be726285a))
* **runtime,codegen:** overflow checks and csv.parse codegen ([#1542](https://github.com/sejihad/EZ/issues/1542), [#1543](https://github.com/sejihad/EZ/issues/1543), [#1546](https://github.com/sejihad/EZ/issues/1546)) ([54f0e76](https://github.com/sejihad/EZ/commit/54f0e7627f6a1c801a04b3c980009558687743d4))
* **runtime:** deep copy maps in copy() builtin ([#1440](https://github.com/sejihad/EZ/issues/1440)) ([5cd75ce](https://github.com/sejihad/EZ/commit/5cd75cee7d3b5a718adfff1b821154c68462cd29))
* **runtime:** encapsulate strings in "" and chars in '' in all print functions ([691d603](https://github.com/sejihad/EZ/commit/691d603437bec6f11924cce20c08f996e82b0488))
* **runtime:** initialize map iterating counter to zero ([#1544](https://github.com/sejihad/EZ/issues/1544)) ([fabcc27](https://github.com/sejihad/EZ/commit/fabcc271ebfa0783d8fdc9a8083a57aa049ea7aa))
* **runtime:** int() and float() panic on invalid string input ([67430d8](https://github.com/sejihad/EZ/commit/67430d882984bf8a8b52e10629e1253187b25604)), closes [#1441](https://github.com/sejihad/EZ/issues/1441)
* **runtime:** panic on map mutation during for_each iteration ([#1544](https://github.com/sejihad/EZ/issues/1544)) ([fa12366](https://github.com/sejihad/EZ/commit/fa12366ef6e254d4afef93f76e1f81de37bc84fc))
* **runtime:** resolve runtime headers when running from subdirectories ([fd817e2](https://github.com/sejihad/EZ/commit/fd817e2e628a74261edf13639016d28add3c85b4))
* **runtime:** zero-initialize arena allocations ([#1539](https://github.com/sejihad/EZ/issues/1539)) ([8075b83](https://github.com/sejihad/EZ/commit/8075b83a76a1876842593a6a336fa136f086b664))
* **stdlib/json:** real recursive-descent validator in json.is_valid ([#1498](https://github.com/sejihad/EZ/issues/1498)) ([200c074](https://github.com/sejihad/EZ/commit/200c074b61d6b0acd5550dfbac8cd5117a6f72f0))
* **stdlib:** fix buffer overflow and missing escaping in #json struct stringify ([#1522](https://github.com/sejihad/EZ/issues/1522)) ([6ce8ae7](https://github.com/sejihad/EZ/commit/6ce8ae72f7bf87e36208474824473af7efd5dc86))
* **stdlib:** remove csv.read and csv.write aliases, keep only read_file/write_file ([#1547](https://github.com/sejihad/EZ/issues/1547)) ([b6a8c27](https://github.com/sejihad/EZ/commit/b6a8c27f1683b891be6b028b2f52a68e695c2ac7))
* **stdlib:** replace fixed buffer estimates with exact sizing in JSON encoders ([#1522](https://github.com/sejihad/EZ/issues/1522)) ([e4fa50a](https://github.com/sejihad/EZ/commit/e4fa50ad49ba6379a6ce32ba640ac872779729cc))
* **stdlib:** validate URL scheme in http module before making requests ([#1555](https://github.com/sejihad/EZ/issues/1555)) ([a00c996](https://github.com/sejihad/EZ/commit/a00c99634c3371b67e17dadd9dc537e488001e2d))
* struct field access, type rewriting, and module detection ([#1406](https://github.com/sejihad/EZ/issues/1406)) ([0e4887d](https://github.com/sejihad/EZ/commit/0e4887d1fbfc1754a0a28a32a6699b216e205dd8))
* struct literal rewriting, mutable var scope ordering, collision detection ([#1406](https://github.com/sejihad/EZ/issues/1406)) ([6a8a57e](https://github.com/sejihad/EZ/commit/6a8a57ea96a956a080b13e322411e734476a8438))
* **tests:** dereference new() pointer in module-prefix-type test ([9bb424b](https://github.com/sejihad/EZ/commit/9bb424bfc2f5b4a5094d15bc77155deaae1fbe11))
* **tests:** update named return e2e test to use explicit mut declarations ([#1560](https://github.com/sejihad/EZ/issues/1560)) ([0f74f6d](https://github.com/sejihad/EZ/commit/0f74f6de57151b482f852c979090dc07d8349c2a))
* transitive and circular imports via iterative while loop ([#1406](https://github.com/sejihad/EZ/issues/1406)) ([a6b3906](https://github.com/sejihad/EZ/commit/a6b39066edcceb26398f802a6a3879e079332f6d))
* transitive import ordering and codegen improvements ([#1406](https://github.com/sejihad/EZ/issues/1406)) ([6b68eac](https://github.com/sejihad/EZ/commit/6b68eac7b48451880f217cf18987896b78f54427))
* type rewriter only rewrites struct/enum types, not primitives ([97a1798](https://github.com/sejihad/EZ/commit/97a179839f3d90ea9a3ecbd80f02a58d6f9649cd))
* **typechecker, codegen:** func ref calls respect default params ([#1503](https://github.com/sejihad/EZ/issues/1503)) ([b624cf7](https://github.com/sejihad/EZ/commit/b624cf711ccfdf03dcb6667e14536511a4ce12e4))
* **typechecker, codegen:** func-typed struct fields visible + callable ([#1505](https://github.com/sejihad/EZ/issues/1505)) ([75c396a](https://github.com/sejihad/EZ/commit/75c396a16bcce1da6996f191fea19585395fedc9))
* **typechecker, codegen:** function-scoped using + proper usage tracking ([#1519](https://github.com/sejihad/EZ/issues/1519) follow-up) ([c84eaa2](https://github.com/sejihad/EZ/commit/c84eaa29230fc703e3be1dbe51886d54e030ef03))
* **typechecker, codegen:** import-and-use brings constants, types, and suppresses false warnings ([#1519](https://github.com/sejihad/EZ/issues/1519)) ([b9c9752](https://github.com/sejihad/EZ/commit/b9c97527a25dd90e3d46364ed42e54fd32ffcf25))
* **typechecker, codegen:** propagate wildcard binding to nested generic calls ([#1506](https://github.com/sejihad/EZ/issues/1506)) ([11e1bc6](https://github.com/sejihad/EZ/commit/11e1bc6be0705b6ca428e62954d5705ee9070cee))
* **typechecker, codegen:** resolve 6 stdlib gaps — register missing functions, fix name mismatches and char codegen ([#1521](https://github.com/sejihad/EZ/issues/1521)) ([e4a7378](https://github.com/sejihad/EZ/commit/e4a7378d4882be7a9517098b32d1e01f975f609c))
* **typechecker, codegen:** wildcard types in map[K:V] params ([#1463](https://github.com/sejihad/EZ/issues/1463)) ([faccf0b](https://github.com/sejihad/EZ/commit/faccf0bb107fc966e39520f4032c5dcc1784d6ca))
* **typechecker,codegen:** fix E3027 for struct functions and [func] var decl ([#1494](https://github.com/sejihad/EZ/issues/1494)) ([22bda46](https://github.com/sejihad/EZ/commit/22bda46d347d4e335d3c8ed40b074c75d273d4ec))
* **typechecker,codegen:** named returns are a contract, not an auto-declaration ([5263f39](https://github.com/sejihad/EZ/commit/5263f39807ce48e884e6cbbf9393a11cc74087eb))
* **typechecker,codegen:** support mutable & params for struct functions and function references ([#1494](https://github.com/sejihad/EZ/issues/1494)) ([76a95d5](https://github.com/sejihad/EZ/commit/76a95d5e3a0b9a08a0775540536c4ccc5f153971))
* **typechecker:** 3 remaining test failures — ref(), enum map keys, multi-file ([125dba2](https://github.com/sejihad/EZ/commit/125dba2f66074ebc0afd70a867dc6e6e72ee2a2f))
* **typechecker:** 9 integration failures from [#1497](https://github.com/sejihad/EZ/issues/1497) whitelist gaps + [#1486](https://github.com/sejihad/EZ/issues/1486) enum carve-outs ([ba98696](https://github.com/sejihad/EZ/commit/ba986966e714d7155712679c5cbd6f7d8a4900d2))
* **typechecker:** accept nil for pointer/Error fields and render pointer types with '^' prefix ([9544b3b](https://github.com/sejihad/EZ/commit/9544b3ba1c1e75e5fccef5e9cc203ab2219c6bb5))
* **typechecker:** add named return hint to E4001 undefined variable ([#1559](https://github.com/sejihad/EZ/issues/1559)) ([8279c8b](https://github.com/sejihad/EZ/commit/8279c8b4a7c840846903acf308cf6b1d729f64c2))
* **typechecker:** allow enum map keys, reject composite keys cleanly ([#1444](https://github.com/sejihad/EZ/issues/1444)) ([3dd0a6d](https://github.com/sejihad/EZ/commit/3dd0a6dc2b1e20edcdc7421b9addd2ee105f0c32))
* **typechecker:** allow multi-var destructuring for fallible stdlib calls ([#1547](https://github.com/sejihad/EZ/issues/1547)) ([afd188e](https://github.com/sejihad/EZ/commit/afd188ef2ecd24e6ecacca1e6f5e823bcc8ed9ab))
* **typechecker:** attribute errors in imported modules to correct source file ([#1491](https://github.com/sejihad/EZ/issues/1491)) ([03ad337](https://github.com/sejihad/EZ/commit/03ad3377a6d5d0200353dba8c56ecda07256b957))
* **typechecker:** broaden E3074/E3076 to cover ordered array/map comparisons ([a13a712](https://github.com/sejihad/EZ/commit/a13a71257521b7cab6423de322cd1303b36c0a0d))
* **typechecker:** broaden E3077 to cover ordered struct comparisons ([a9da673](https://github.com/sejihad/EZ/commit/a9da673a11270d46d665ed654ea6383f4628f269))
* **typechecker:** catch non-array first argument in arrays.append/prepend/insert_at ([30f9df4](https://github.com/sejihad/EZ/commit/30f9df48c5a0e09a23ed7cd0a8e98199d5c108c4))
* **typechecker:** coerce main() to void after E4008 to suppress cascade ([#1482](https://github.com/sejihad/EZ/issues/1482)) ([fe3ec91](https://github.com/sejihad/EZ/commit/fe3ec914a852fa97fe5f879386338f1a7ab75c7a))
* **typechecker:** collapse invalid infix result to TK_UNKNOWN to stop cascades ([#1488](https://github.com/sejihad/EZ/issues/1488)) ([7663d9d](https://github.com/sejihad/EZ/commit/7663d9d74cabe312a22593750085deed8154a659))
* **typechecker:** detect bare function names used as statements (E3081) ([d0f2f5c](https://github.com/sejihad/EZ/commit/d0f2f5ce1e0fcea7c03eac0cf282571bc423ddf9))
* **typechecker:** E3036 range check on reassignment + struct field assignment ([#1515](https://github.com/sejihad/EZ/issues/1515)) ([35a87ba](https://github.com/sejihad/EZ/commit/35a87ba8b2fe0a57048bf15a1dbf8efe7f2812ea))
* **typechecker:** E3053 on map literal key/value type mismatch ([#1486](https://github.com/sejihad/EZ/issues/1486)) ([834e780](https://github.com/sejihad/EZ/commit/834e7805981e748a936480ad78adcc2e7c94303a))
* **typechecker:** emit E4005 for unknown stdlib function names ([#1497](https://github.com/sejihad/EZ/issues/1497)) ([c8736fb](https://github.com/sejihad/EZ/commit/c8736fb94c58c9fc38b8da2447765fe84e27e3e8))
* **typechecker:** emit W2011 for unused named return values ([#1556](https://github.com/sejihad/EZ/issues/1556)) ([14fb474](https://github.com/sejihad/EZ/commit/14fb474493f4c36c242b29bba53b4bf2988a4e83))
* **typechecker:** enforce named return variables must be returned (E3080) ([dcfc396](https://github.com/sejihad/EZ/commit/dcfc3963a8415781a4cce5d59278ff1f6024284c))
* **typechecker:** give each when/is branch its own scope ([#1560](https://github.com/sejihad/EZ/issues/1560)) ([2829ca6](https://github.com/sejihad/EZ/commit/2829ca6532ae3abcac0b3b50bf89a2d2c5f4db47))
* **typechecker:** instance dispatch for &self struct methods ([#1509](https://github.com/sejihad/EZ/issues/1509)) ([95efc38](https://github.com/sejihad/EZ/commit/95efc38abf8105d7dc7ea95faa6a8c3cfe52c7c1))
* **typechecker:** mark module used when its types appear in annotations ([647a88b](https://github.com/sejihad/EZ/commit/647a88b888f6fc378598fd8b2b43ffdd8e941805))
* **typechecker:** prevent duplicate diagnostics on re-resolved expressions ([#1485](https://github.com/sejihad/EZ/issues/1485)) ([1477d91](https://github.com/sejihad/EZ/commit/1477d9169688bca8e380d9e6308db2ba35bf86dd))
* **typechecker:** recognize return inside loop as valid return path ([c9e361e](https://github.com/sejihad/EZ/commit/c9e361ee9532ff54f825a9d8469289b999236d6f)), closes [#1427](https://github.com/sejihad/EZ/issues/1427)
* **typechecker:** recover [func] array element return type at call site ([#1458](https://github.com/sejihad/EZ/issues/1458)) ([18845b6](https://github.com/sejihad/EZ/commit/18845b6778c484945790fc6b965504386a5a72de))
* **typechecker:** reject 'return nil' from non-nullable return types ([76e95d0](https://github.com/sejihad/EZ/commit/76e95d02a4e688583daec4776f8e40e7148037bd))
* **typechecker:** reject `return nil` from a wildcard-return function ([6e5df45](https://github.com/sejihad/EZ/commit/6e5df4547d0f02a3b008a04060f75a8273f97c52))
* **typechecker:** reject array literal assigned to map variable ([#1477](https://github.com/sejihad/EZ/issues/1477)) ([ee0b4d4](https://github.com/sejihad/EZ/commit/ee0b4d487e9bc2634968375f2c8343a2f39e2d39))
* **typechecker:** reject bare function name used as value ([#1475](https://github.com/sejihad/EZ/issues/1475)) ([aba3e98](https://github.com/sejihad/EZ/commit/aba3e98236dfdc20ea3e52871bc0285f2267c146))
* **typechecker:** reject by-value self-referential structs ([#1489](https://github.com/sejihad/EZ/issues/1489)) ([cdff0ca](https://github.com/sejihad/EZ/commit/cdff0ca29bd287f0dae0865e59cd3d4d4d476ed5))
* **typechecker:** reject chained struct function calls cleanly with E3075 ([a90bffd](https://github.com/sejihad/EZ/commit/a90bffd6da332f2fcf3801806d00bd08a5e38923))
* **typechecker:** reject const declaration on maps ([#1468](https://github.com/sejihad/EZ/issues/1468)) ([ba6177b](https://github.com/sejihad/EZ/commit/ba6177b7d4d0a53e266153f0bf0c08148918be94))
* **typechecker:** reject const on channel/mutex/thread handles ([#1480](https://github.com/sejihad/EZ/issues/1480)) ([522090b](https://github.com/sejihad/EZ/commit/522090bd37f499d00c7fc1cb85c5e27579dc01e8))
* **typechecker:** reject cross-enum assignment ([#1471](https://github.com/sejihad/EZ/issues/1471)) ([0f962e5](https://github.com/sejihad/EZ/commit/0f962e5123a80aec313360298ce09ae491d2792f))
* **typechecker:** reject func-typed variables in string interpolation ([#1554](https://github.com/sejihad/EZ/issues/1554)) ([f139fee](https://github.com/sejihad/EZ/commit/f139feeb07bfb20d73165cd8700a00bc85d2c74c))
* **typechecker:** reject inline enum declarations with E2053 ([#1521](https://github.com/sejihad/EZ/issues/1521)) ([1028103](https://github.com/sejihad/EZ/commit/1028103d99d1acc9b4a02bab18084f357268e383))
* **typechecker:** reject int → enum assignment and return ([#1472](https://github.com/sejihad/EZ/issues/1472)) ([80b307b](https://github.com/sejihad/EZ/commit/80b307bb174999ef0dbe97662b3c874c163dfeed))
* **typechecker:** reject literal divide/modulo by zero at compile time ([#1474](https://github.com/sejihad/EZ/issues/1474)) ([a763f47](https://github.com/sejihad/EZ/commit/a763f47cd09a281dd3e6d6da04b21d54832388f7))
* **typechecker:** reject literals and expressions passed to mutable params ([#1493](https://github.com/sejihad/EZ/issues/1493)) ([486dbd9](https://github.com/sejihad/EZ/commit/486dbd934705309bd45a3aa8f41cf079e8d6d5e5))
* **typechecker:** reject mutable reference to const source with E3079 ([a648e5f](https://github.com/sejihad/EZ/commit/a648e5fdfad4c3e13c6c768d9295bc81980cceb8))
* **typechecker:** reject mutations on const arrays/maps, negative array index ([98ecf99](https://github.com/sejihad/EZ/commit/98ecf9966e291317a52bc5912a5a09af94d86c8d))
* **typechecker:** reject negative literal index on strings ([#1500](https://github.com/sejihad/EZ/issues/1500)) ([45a0ea5](https://github.com/sejihad/EZ/commit/45a0ea589a5e98fa4b84406de8291fe9c75487f0))
* **typechecker:** reject nested 'ensure' instead of silently dropping ([96d944e](https://github.com/sejihad/EZ/commit/96d944eb0e2435f2854be415ad0d38739a02c594))
* **typechecker:** reject nil assignment to non-nullable types ([211a51d](https://github.com/sejihad/EZ/commit/211a51d453431e8f3b09ee36ac0027682ba9a188)), closes [#1436](https://github.com/sejihad/EZ/issues/1436)
* **typechecker:** reject nil in non-equality operators ([#1487](https://github.com/sejihad/EZ/issues/1487)) ([aebbef7](https://github.com/sejihad/EZ/commit/aebbef71d8891fc34f609c7694d6d61a99c1df21))
* **typechecker:** reject non-func value for 'func' var ([#1479](https://github.com/sejihad/EZ/issues/1479)) ([88f3a72](https://github.com/sejihad/EZ/commit/88f3a72a438e6776fa25699d0ebdad197bdf21b9))
* **typechecker:** reject non-socket arguments to net.send/receive/close/accept ([#1547](https://github.com/sejihad/EZ/issues/1547)) ([11df53d](https://github.com/sejihad/EZ/commit/11df53d94695ebc443aece50c3c4a75c06a0894a))
* **typechecker:** reject pointer arithmetic with E3078 ([c299d71](https://github.com/sejihad/EZ/commit/c299d717e0401c558695bd1f4d4b451aa7a08f0f))
* **typechecker:** reject pointer depth mismatch on return ([#1514](https://github.com/sejihad/EZ/issues/1514)) ([9ce6aa1](https://github.com/sejihad/EZ/commit/9ce6aa111342699e406ba7dda3561318c872b046))
* **typechecker:** reject string argument to csv.write/write_file ([#1547](https://github.com/sejihad/EZ/issues/1547)) ([856423e](https://github.com/sejihad/EZ/commit/856423ed8de7d20d8cbd064deae9cc414ff81a42))
* **typechecker:** reject struct / pointer / func in string interpolation ([#1499](https://github.com/sejihad/EZ/issues/1499)) ([5ee97e4](https://github.com/sejihad/EZ/commit/5ee97e4ff0e7a6dc9fdc9b9dbe044dd63fb1b050))
* **typechecker:** reject struct == / != with E3077 ([bc317b3](https://github.com/sejihad/EZ/commit/bc317b3acbec1bceac2fa18874abab39017937f9))
* **typechecker:** reject void call in if/or/as_long_as condition ([#1476](https://github.com/sejihad/EZ/issues/1476)) ([d73135b](https://github.com/sejihad/EZ/commit/d73135b135c9872e70260e0294658a8f8a20297c))
* **typechecker:** reject wildcard return type with no wildcard params ([#1469](https://github.com/sejihad/EZ/issues/1469)) ([23621fa](https://github.com/sejihad/EZ/commit/23621faa85ae865ec274dabf8b86228979298029))
* **typechecker:** reject wildcard type '?' in named return positions ([#1557](https://github.com/sejihad/EZ/issues/1557)) ([34e1d36](https://github.com/sejihad/EZ/commit/34e1d3602a9b4d0331efb7b71cae1233114747d5))
* **typechecker:** reject wrong enum type as function argument ([#1473](https://github.com/sejihad/EZ/issues/1473)) ([a346539](https://github.com/sejihad/EZ/commit/a3465397825cb96d04ea6945642c800acdbabb3c))
* **typechecker:** remove implicit pointer-to-value type coercion ([017fd21](https://github.com/sejihad/EZ/commit/017fd2196697792ecfcf7e98be3b66a741f6ada1))
* **typechecker:** replace cast blocklist with allowlist validation ([#1525](https://github.com/sejihad/EZ/issues/1525)) ([aa7a540](https://github.com/sejihad/EZ/commit/aa7a5409f6daa371756120c9d4bea7f19b10707f))
* **typechecker:** resolve enum field types correctly in imported structs ([#1492](https://github.com/sejihad/EZ/issues/1492)) ([24d3e6f](https://github.com/sejihad/EZ/commit/24d3e6f442614558124f129664798b1ffbb03ffa))
* **typechecker:** resolve non-label call targets so subtrees get typed ([#1439](https://github.com/sejihad/EZ/issues/1439)) ([1a3e7c6](https://github.com/sejihad/EZ/commit/1a3e7c6e9ee44fc9015b03eb1825c31e9c1c6398))
* **typechecker:** resolve return type from typed [func] array element type ([#1558](https://github.com/sejihad/EZ/issues/1558)) ([e43c616](https://github.com/sejihad/EZ/commit/e43c616ca9de27ebd722e8ea20b3f5d318110c85))
* **typechecker:** resolve struct types in multi-var destructuring for stdlib ([#1547](https://github.com/sejihad/EZ/issues/1547)) ([307e671](https://github.com/sejihad/EZ/commit/307e67109fb9fb35c28e01f06fd7a81b6c705aa9))
* **typechecker:** resolve struct types in multi-var destructuring for stdlib ([#1547](https://github.com/sejihad/EZ/issues/1547)) ([e35d15b](https://github.com/sejihad/EZ/commit/e35d15bb0f36a7b44919c5af2a9af5eed67c7b99))
* **typechecker:** substitute wildcard binding into multi-return slot types ([084b282](https://github.com/sejihad/EZ/commit/084b282db29712da6b62ffbda25fbb5d6e304fe6))
* **typechecker:** suppress cascading E3060 when E3082 covers named wildcard returns ([#1557](https://github.com/sejihad/EZ/issues/1557)) ([250dd7d](https://github.com/sejihad/EZ/commit/250dd7dbaceaad01a29950d9ba563873c371174e))
* **typechecker:** tighten lvalue check on addr() and ref(); reject rvalue chains ([af0fab3](https://github.com/sejihad/EZ/commit/af0fab36f124fcbe54be7c1e9974b190068a21ee))
* **typechecker:** track func_array_refs for typed [func] arrays ([#1553](https://github.com/sejihad/EZ/issues/1553)) ([eea0af9](https://github.com/sejihad/EZ/commit/eea0af9ee653aa419bafe905a84c20e1c5cac237))
* **typechecker:** validate argument types for instance-dispatched struct function calls ([#1526](https://github.com/sejihad/EZ/issues/1526)) ([2123901](https://github.com/sejihad/EZ/commit/2123901c5fe5e645c5519663a14e5b79f959b52f))
* **typechecker:** validate c_string() argument is a pointer type ([#1575](https://github.com/sejihad/EZ/issues/1575)) ([f780f87](https://github.com/sejihad/EZ/commit/f780f87cab185e27b31c25a8f04dcf67ea06f7f0))
* **typechecker:** validate calls through func-typed vars ([#1437](https://github.com/sejihad/EZ/issues/1437)) ([2a35462](https://github.com/sejihad/EZ/commit/2a35462295ca8f67151200c9766904eca3899388))
* **typechecker:** validate len() argument type ([#1490](https://github.com/sejihad/EZ/issues/1490)) ([c117ffe](https://github.com/sejihad/EZ/commit/c117ffe266099ec6e4d17395c212a27aa50e7056))
* **typechecker:** W1005 wording points at the actually-valid form ([#1501](https://github.com/sejihad/EZ/issues/1501)) ([1fe6b35](https://github.com/sejihad/EZ/commit/1fe6b3545ad5b0b940fac403429f294279af7ab4))
* typeof test — convert inline enum to multiline format ([#1410](https://github.com/sejihad/EZ/issues/1410)) ([5639e56](https://github.com/sejihad/EZ/commit/5639e56728d2bc368cc458b9aa33fa6572fcbde6))
* **types:** reject 'void' in typed-func return position ([75920ef](https://github.com/sejihad/EZ/commit/75920ef99d4b63cc8b3c0272bb0de853a5b48e5a))
* uint precision — carry full UINT64_MAX range end-to-end ([ecac542](https://github.com/sejihad/EZ/commit/ecac542e9de7a7b8f11f6cf7a4e51df7a6f2e530))
* update 3 typechecker tests — W2001→W1002, multiline struct/enum format ([18ac4b1](https://github.com/sejihad/EZ/commit/18ac4b1366cacd46e8a381343a17435a915abbf5))
* update 6 e2e tests for inline struct/enum rejection and arrays rename ([cfe81e8](https://github.com/sejihad/EZ/commit/cfe81e8186b029952e8049e5c4b55e0666210ba6))
* update 8 stress tests for v3 API changes ([8663f41](https://github.com/sejihad/EZ/commit/8663f41ebc4297adabcfd4839b04a519b902a07b))


### Reverts

* remove nullable pointer syntax (?^T) from [#1521](https://github.com/sejihad/EZ/issues/1521) ([04e09e5](https://github.com/sejihad/EZ/commit/04e09e516896eefc6f53b1062fdea0223139bfc4))

## [3.0.0](https://github.com/SchoolyB/EZ/compare/v2.0.0...v3.0.0) (2026-04-28)

EZ 3.0 is a "from the ground up rewrite". The Go-based interpreter has been replaced by a **compiled backend** that emits C and produces native binaries. Every stage of the pipeline — lexer, parser, typechecker, and code generator is now written in C. The Go CLI remains as the user-facing tooling wrapper.

### Breaking Changes

- **Compiled, not interpreted.** EZ programs now compile to native binaries via C. The Go interpreter is gone.
- **`@std` module removed.** All former `@std` functions (`println`, `print`, `len` `input`, `assert`, `panic`, `exit`, etc.) are now **builtins** — always available, no import needed.
- **`module` keyword removed.** Modules are identified by their filesystem path. Using `module` now produces E2061.
- **`#suppress` attribute removed.** Warning suppression moved to the CLI: `ez build -q W1001,W2003`.
- **`#enum(type)` attribute removed.** Enum variants are always integer-valued.
- **`nil` is no longer a type.** `nil` is a value only — use `Error`, pointer types, or optionals for nullability.
- **`ez run` removed.** Compile and run files directly with `ez <file.ez>`.
- **`temp` renamed to `mut`.** All mutable variable declarations now use `mut`.
- **`import & use` syntax replaced** by `import and use`. The `&` shorthand no longer works.
- **`new()` now returns a pointer.** `new(StructName)` returns `^Struct`, not a value.
- **`bare func` type removed.** Function references require full signatures: `func(int, int) -> int`.
- **`sleep_s`, `sleep_ms`, `sleep_ns` moved from time module to builtins.**
- **Many more!**

### New Features

**Compiler & Type System**
- Native compilation via C backend source to binary in one step
- Scope-based automatic memory management — every scope gets its own arena allocator. Allocations are freed when the scope exits. Values that escape (via return, outer assignment, or container storage) are automatically copied to the parent scope. No garbage collector, no manual free for normal code.
- Overflow-checked integer arithmetic at runtime
- Division-by-zero runtime checks
- Wildcard type `?` for generic-style functions monomorphised per call site
- Implicit int-to-float coercion in assignments, arguments, and returns
- `private` keyword for functions and constants
- Named return values in function signatures
- Default parameter values for functions
- Struct functions — functions defined inside structs with instance dispatch (`point.distance()`)
- `for_each i, item in arr` — index-value destructuring for arrays
- `for_each k, v in myMap` — key-value destructuring for maps
- `while` keyword as an alias for `as_long_as`
- `#json` attribute for struct-based JSON serialization/deserialization
- Wildcard struct fields
- `or_return` for error propagation

**Pointers**
- `^Type` pointer syntax — e.g. `^int`, `^Point`
- `new(StructName)` now returns a `^Struct` pointer to a heap-allocated struct
- `addr(variable)` returns the memory address of a variable as a pointer
- Dereference pointers with `p^`
- Auto-deref for struct field access — `ptr.field` works without explicit deref
- Pointer comparison limited to `==`/`!=` with `nil` only. No pointer arithmetic

**Functions as First-Class Types**
- `func` is a type — functions can be stored in variables, passed as arguments, and returned from functions
- Full signature syntax: `func(int, int) -> int`
- `()func` call syntax for invoking function references

**Breaking: `temp` renamed to `mut`**
- The `temp` keyword for mutable variables is now `mut`

**New Builtins**
- `sleep_s()`, `sleep_ms()`, `sleep_ns()` — sleep functions (formerly in the @time module, now builtins)
- `addr()` — returns a pointer to a variable

**Wide Integer Types**
- `i256`, `u256` — new wide integer sizes
- `i128`, `u128` — reimplemented as portable struct-based types (previously interpreter-only)

**C Interop**
- `import c"header.h"` to include C headers
- Call C functions via `c.func()` syntax
- `c_string()` builtin to convert C `char*` back to EZ strings
- Access C constants via `c.CONSTANT`
- Type mapping between EZ and C primitives

**Module System**
- Filesystem-based module identity (directory name = module name)
- Directory imports merge all `.ez` files into one namespace
- Import aliasing: `import m @math`
- `import and use` combined syntax (replaces the former `import & use`)
- Module-qualified struct literals: `lib.Point{x: 1}`
- Module-qualified enum access
- Extensionless file and directory imports
- Transitive imports and import caching
- Duplicate module name detection with E6001

**Standard Library**

All 27 stdlib modules now run on the compiled C backend. Modules that existed in the v2 interpreter (`@http`, `@server`, `@regex`, `@csv`, `@threads`, etc.) have been reimplemented in C.

New modules:
- `@net` — TCP sockets and DNS
- `@atomic` — lock-free assembly-backed operations (x86_64 + ARM64)
- `@mem` — manual arena-based memory management
- `@fmt` — formatted output, padding, number formatting
- `@sync` — mutexes (split from former `@threads`)
- `@channels` — typed channels (split from former `@threads`)

Notable changes to existing modules:
- `@io` — added 23 filesystem and path manipulation functions
- All fallible stdlib functions now have `_result` variants that return `(T, Error)` instead of panicking
- `to_char()` and `char_count()` builtins for Unicode codepoint access

**CLI Tooling**

New commands:
- `ez report` — system info for bug reports (OS, CPU, RAM, C compiler, install path)
- `ez test` — unified test runner with aggregated counts
- `ez install <version>` — pin to a specific version

New flags:
- `--pre` — install pre-release versions via `ez update --pre`
- `-q` / `--quiet` — suppress warnings (global or per-code, e.g. `-q W1001,W2003`)
- `--no-color` — plain output without ANSI colors
- `--emit-c` — inspect the generated C source
- `--time` — show compilation timing

Other changes:
- Single embedded binary — `ezc` compiler and runtime are embedded in the `ez` binary, no separate install needed
- `ez version` now shows installed, latest stable, and latest pre-release

**Error System**
- Centralized error code registry (`error_codes.h`) with auto-generated `ERRORS.md`
- Rust-inspired diagnostics: error code, message, source location, caret pointing, optional help hints
- 100+ compile-time error checks across lexer, parser, typechecker
- Warning system with per-code suppression
- Runtime panics with file/line/column info for division-by-zero, nil deref, array OOB, stack overflow

**Testing & CI**
- 1,200+ tests: unit (C), end-to-end, integration (pass + fail + warning + stress + multi-file)
- UBSan and ASan sanitizer builds in CI

---

## [2.0.0](https://github.com/SchoolyB/EZ/compare/v1.4.9...v2.0.0) (2026-02-14)


### ⚠ BREAKING CHANGES

* The lowercase `error` type alias has been removed. Use `Error` (capitalized) for type annotations instead.

### Features

* add [@server](https://github.com/server) HTTP server stdlib module ([#439](https://github.com/SchoolyB/EZ/issues/439)) ([acd7f16](https://github.com/SchoolyB/EZ/commit/acd7f162813fb9b9fbf950f06f291dd810b39a4d))
* add #doc attribute and ez doc command for documentation generation ([2d26a37](https://github.com/SchoolyB/EZ/commit/2d26a37f7dfc11c689b7b506cb5a77164f9a88b9)), closes [#764](https://github.com/SchoolyB/EZ/issues/764)
* add `[@server](https://github.com/server)` HTTP server stdlib module ([bc6d815](https://github.com/SchoolyB/EZ/commit/bc6d815dae237dd0e7271a412ad9b7a15c315100))
* add `ez pz` project scaffolding command ([a422c15](https://github.com/SchoolyB/EZ/commit/a422c15be13cc8b01c084fdd8beee685b219f44f))
* add `ez pz` project scaffolding command ([a1adcc0](https://github.com/SchoolyB/EZ/commit/a1adcc0f4381a5d6e160ca7c329301aa46608738))
* Add named return variables support ([#1131](https://github.com/SchoolyB/EZ/issues/1131)) ([6e4d70e](https://github.com/SchoolyB/EZ/commit/6e4d70ee910d6088fddd7d778e5157516a978d23))
* add optional index variable to `for_each` loops ([#1139](https://github.com/SchoolyB/EZ/issues/1139)) ([7a8a5a2](https://github.com/SchoolyB/EZ/commit/7a8a5a26a41df5343e928bf41c1807a01149bbc6))
* add optional index variable to for_each loops ([#1139](https://github.com/SchoolyB/EZ/issues/1139)) ([4b0378d](https://github.com/SchoolyB/EZ/commit/4b0378d859fc3c766f74fc235296316f4e2742ef))
* add server and client templates to ez pz scaffolding ([9f873bf](https://github.com/SchoolyB/EZ/commit/9f873bf51577aceff8834defb5ac093076cf2332))
* **cmd:** add `ez watch` command for live reloading ([741c279](https://github.com/SchoolyB/EZ/commit/741c2790c981d2619c929542a31433e663058e96))
* **cmd:** add `ez watch` command for live reloading ([4910b73](https://github.com/SchoolyB/EZ/commit/4910b733e64128046af203ee8ac58b53db29df95)), closes [#871](https://github.com/SchoolyB/EZ/issues/871)
* **errors:** add color formatting to parser, evaluator, and stdlib error messages ([#810](https://github.com/SchoolyB/EZ/issues/810)) ([cc9748f](https://github.com/SchoolyB/EZ/commit/cc9748f8f2370365b3c8a81ec69e4b9a13969f38))
* **errors:** add color formatting to remaining stdlib module error messages ([#810](https://github.com/SchoolyB/EZ/issues/810)) ([9b666d1](https://github.com/SchoolyB/EZ/commit/9b666d124d972b12c185c18228e9e337908dd242))
* **errors:** add color formatting to typechecker error messages ([837c258](https://github.com/SchoolyB/EZ/commit/837c258b4ef31e293b2a12cec549d284a228e7ec))
* **errors:** add color formatting to typechecker error messages ([#810](https://github.com/SchoolyB/EZ/issues/810)) ([023914a](https://github.com/SchoolyB/EZ/commit/023914a6a4a25dd54ff88f49697ffb8583dcc879))
* **loader:** add multi-file main module support ([fe0335e](https://github.com/SchoolyB/EZ/commit/fe0335e73e2fd183937876c366a3f8e8288ef0e1))
* **parser:** add named return variables support ([#1131](https://github.com/SchoolyB/EZ/issues/1131)) ([a1eea1c](https://github.com/SchoolyB/EZ/commit/a1eea1cc81bfe2cd1e826db94c433b4ac6a66d8d))
* **stdlib/csv:** add [@csv](https://github.com/csv) module for reading and writing CSV files ([4ec274b](https://github.com/SchoolyB/EZ/commit/4ec274b1e0650a2ca2fd2ea7e7f05bcf130000b6))
* **stdlib/csv:** add [@csv](https://github.com/csv) module for reading and writing CSV files ([d6af096](https://github.com/SchoolyB/EZ/commit/d6af09690cc43a49acc380c8e0efab8a7d204f57)), closes [#965](https://github.com/SchoolyB/EZ/issues/965)
* **stdlib/math:** add NaN/finite checks and float constants ([#1123](https://github.com/SchoolyB/EZ/issues/1123)) ([b22667b](https://github.com/SchoolyB/EZ/commit/b22667b77687f5045496daaa364e7ab589de307f)), closes [#1024](https://github.com/SchoolyB/EZ/issues/1024)
* **stdlib/regex:** add [@regex](https://github.com/regex) module for regular expression operations ([de8063c](https://github.com/SchoolyB/EZ/commit/de8063c379cd3d0b873264196d21696714a55105))
* **stdlib/regex:** add `[@regex](https://github.com/regex)` module for regular expression operations ([931bdcc](https://github.com/SchoolyB/EZ/commit/931bdccd0bcc475db594414762637b2f007e2338))
* **stdlib/strings:** add 12 new string utility functions ([6cb2a2d](https://github.com/SchoolyB/EZ/commit/6cb2a2df0f166cd041df37f2af47122cbebb18ed))
* **stdlib/strings:** add 12 new string utility functions ([a4ad38f](https://github.com/SchoolyB/EZ/commit/a4ad38f2bfb8009a0ee4a9ad4afbde0a3264b699)), closes [#1020](https://github.com/SchoolyB/EZ/issues/1020)
* **typechecker:** add W1005 warning for typed blank identifiers ([b9a4c62](https://github.com/SchoolyB/EZ/commit/b9a4c623844bb089a0520c1f19343942c85e10c9))
* **typechecker:** add W1005 warning for typed blank identifiers ([df1a334](https://github.com/SchoolyB/EZ/commit/df1a3346653255083b305933df394855587c0b29))


### Bug Fixes

* add encoding module to multi-return type inference ([#1138](https://github.com/SchoolyB/EZ/issues/1138)) ([23d806b](https://github.com/SchoolyB/EZ/commit/23d806b4fbb9f800eecb50afe1c19b1f5f508b54))
* allow enum constants in `when/is` when value is explicitly typed ([#1143](https://github.com/SchoolyB/EZ/issues/1143)) ([03e99d3](https://github.com/SchoolyB/EZ/commit/03e99d3a8c278401430cadb426d6971d5533480a))
* allow enum constants in when/is when value is explicitly typed ([#1143](https://github.com/SchoolyB/EZ/issues/1143)) ([1832e66](https://github.com/SchoolyB/EZ/commit/1832e66d5106bb109b05b05f3201bc225d6eef93))
* arrays.join no longer wraps string elements in quotes ([#1144](https://github.com/SchoolyB/EZ/issues/1144)) ([5b9c1a3](https://github.com/SchoolyB/EZ/commit/5b9c1a35df238beafee9b45eb526b517a2e71ae6))
* clarify misleading error messages in json.decode, db module, and typechecker ([028359b](https://github.com/SchoolyB/EZ/commit/028359bd9a03a82044c9ecb4d2a6d851f7580ae4))
* complete tuple type inference for all stdlib modules ([#1138](https://github.com/SchoolyB/EZ/issues/1138)) ([2c30882](https://github.com/SchoolyB/EZ/commit/2c30882f4a0c141b4eba85ea44d21f398bb6406f))
* eliminate race condition by removing global eval state ([#1122](https://github.com/SchoolyB/EZ/issues/1122)) ([e17f686](https://github.com/SchoolyB/EZ/commit/e17f68618a0ca39d8fd58c5ab54e6f24e9e6c26e)), closes [#949](https://github.com/SchoolyB/EZ/issues/949)
* **interpreter:** use correct error code E5011 for unused return values ([116ba16](https://github.com/SchoolyB/EZ/commit/116ba1652aa9c9a2c68e286831c774fde553d987))
* **language:** remove extra quotes from string enum casting ([70aeac2](https://github.com/SchoolyB/EZ/commit/70aeac26b2c3c4d5d5b323ba8c812985c4625f82))
* nested array types in multi-return declarations ([#1137](https://github.com/SchoolyB/EZ/issues/1137)) ([3186097](https://github.com/SchoolyB/EZ/commit/31860970dfe9e314de50f0a1e15b4c9362b6ae0f))
* **parser,typechecker:** fix #suppress attribute not working ([cb216a2](https://github.com/SchoolyB/EZ/commit/cb216a22dccbc64c4ad31b84798e118e4a33a6a2))
* **parser:** use user-friendly descriptions in assignment error messages ([e9d8d41](https://github.com/SchoolyB/EZ/commit/e9d8d419faf05410c36076b28c988fae7b8077fd))
* **parser:** validate #doc attribute placement ([e34198c](https://github.com/SchoolyB/EZ/commit/e34198c21111355d56a751f00c717b00be8eff1d))
* **parser:** validate `#doc` attribute placement ([01f9ef5](https://github.com/SchoolyB/EZ/commit/01f9ef5a7877c6e9e6a171283c17e716079832b1))
* **pz:** correct EZ syntax in project scaffolding templates ([ff51760](https://github.com/SchoolyB/EZ/commit/ff5176070553fe1c98f9a1f4cab435905ed6ea21))
* remove lowercase `error` type alias, keep only `Error` ([cc2c36f](https://github.com/SchoolyB/EZ/commit/cc2c36f0fa57429248f63b5aab5173dd305cd360)), closes [#1039](https://github.com/SchoolyB/EZ/issues/1039)
* respect explicit type annotations in multi-return declarations ([#1137](https://github.com/SchoolyB/EZ/issues/1137)) ([e3838fc](https://github.com/SchoolyB/EZ/commit/e3838fcde532faba9f18308de3c78b28f801c3e8))
* **stdlib/arrays:** `arrays.join` no longer wraps string elements in quotes ([#1144](https://github.com/SchoolyB/EZ/issues/1144)) ([333f53e](https://github.com/SchoolyB/EZ/commit/333f53e5868d10bff33db4ebbb414c0c778ceddd))
* **stdlib:** correct test expectations to match implementation ([58478b3](https://github.com/SchoolyB/EZ/commit/58478b33f45cde3501ef13ff66f85c4cbcca6830))
* **typechecker:** disallow function calls in file-scope variable initializers ([1d78de8](https://github.com/SchoolyB/EZ/commit/1d78de8ab4f408f2df84d565708940bf720119e1))
* **typechecker:** prevent W2010 false positive on nested struct initialization ([f7058b0](https://github.com/SchoolyB/EZ/commit/f7058b0d46ce439a8b2bf5855ccd01be42c135b0))
* **typechecker:** prevent W2010 false positive on nested struct initialization ([7d25b8a](https://github.com/SchoolyB/EZ/commit/7d25b8af31715f7df9e3a9f2ca3ccaea06646d7d)), closes [#1107](https://github.com/SchoolyB/EZ/issues/1107)

## [1.4.9](https://github.com/SchoolyB/EZ/compare/v1.4.8...v1.4.9) (2026-02-04)


### Bug Fixes

* multiple bug fixes for type inference and expressions ([f3853dd](https://github.com/SchoolyB/EZ/commit/f3853dde73565115af45f3487ec76a88fcad80ae))
* multiple bug fixes for type inference and expressions ([0817610](https://github.com/SchoolyB/EZ/commit/081761062e0f02498b38692ac4d98caf717ae7f6))

## [1.4.8](https://github.com/SchoolyB/EZ/compare/v1.4.7...v1.4.8) (2026-01-30)


### Bug Fixes

* `range()`, module imports, and error file tracking ([#1093](https://github.com/SchoolyB/EZ/issues/1093), [#1094](https://github.com/SchoolyB/EZ/issues/1094), [#1095](https://github.com/SchoolyB/EZ/issues/1095)) ([331b0b4](https://github.com/SchoolyB/EZ/commit/331b0b4eb0a0c4a1bde7771432c088e85f480953))
* mark modules as used when referenced in type annotations ([#1093](https://github.com/SchoolyB/EZ/issues/1093)) ([#1096](https://github.com/SchoolyB/EZ/issues/1096)) ([6aa9a24](https://github.com/SchoolyB/EZ/commit/6aa9a2420938b399c7763b65b50ec37e5d94677b))
* set correct file in runtime errors from builtin functions ([#1094](https://github.com/SchoolyB/EZ/issues/1094)) ([#1097](https://github.com/SchoolyB/EZ/issues/1097)) ([9f41400](https://github.com/SchoolyB/EZ/commit/9f414000683eaec7b106f1c42abdcc36d7437e5f))
* support negative step in range() for backwards iteration ([#1095](https://github.com/SchoolyB/EZ/issues/1095)) ([#1098](https://github.com/SchoolyB/EZ/issues/1098)) ([b12e474](https://github.com/SchoolyB/EZ/commit/b12e474609feaa47c6751dda4411295db3b30312))

## [1.4.7](https://github.com/SchoolyB/EZ/compare/v1.4.6...v1.4.7) (2026-01-30)


### Bug Fixes

* const ref now creates read-only view of referenced value ([#1089](https://github.com/SchoolyB/EZ/issues/1089)) ([4b04eed](https://github.com/SchoolyB/EZ/commit/4b04eedf59f422fa1b786c819c9d2920acd4395d))
* mutability semantics fixes ([b88a35e](https://github.com/SchoolyB/EZ/commit/b88a35ea0be3720e177d8c06dfa173dd2f880014))
* support const keyword with multi-return function assignment ([#1087](https://github.com/SchoolyB/EZ/issues/1087)) ([2375f3c](https://github.com/SchoolyB/EZ/commit/2375f3c6ada883e8426b9e02d3ff44722f9e8878))
* sync temp/const mutability with value's Mutable field ([#1085](https://github.com/SchoolyB/EZ/issues/1085)) ([5f0ffb7](https://github.com/SchoolyB/EZ/commit/5f0ffb78b66d794d5da802f3c558e527d0c0c0a4))

## [1.4.6](https://github.com/SchoolyB/EZ/compare/v1.4.5...v1.4.6) (2026-01-29)


### Bug Fixes

* arrays module bugs - remove() deleted, remove_at() now in-place ([#1083](https://github.com/SchoolyB/EZ/issues/1083)) ([92e224e](https://github.com/SchoolyB/EZ/commit/92e224ee1cec5a067f9c105d780c34690bb17b59))

## [1.4.5](https://github.com/SchoolyB/EZ/compare/v1.4.4...v1.4.5) (2026-01-29)


### Bug Fixes

* allow empty arrays as elements when type is explicitly declared ([#1076](https://github.com/SchoolyB/EZ/issues/1076)) ([9c7be92](https://github.com/SchoolyB/EZ/commit/9c7be9274dada568d7125af088521f66db3a235b)), closes [#1064](https://github.com/SchoolyB/EZ/issues/1064)
* bugfixes 1-29-2026 ([8c0980a](https://github.com/SchoolyB/EZ/commit/8c0980aae9ec5931d42c9c98775ff7dae375e98b))
* expand 'did you mean?' suggestions across typechecker errors ([#1075](https://github.com/SchoolyB/EZ/issues/1075)) ([3dfcee3](https://github.com/SchoolyB/EZ/commit/3dfcee348716261d545cc403d09e036dc91dbc3a))
* handle file close error explicitly in io.copy ([44ea553](https://github.com/SchoolyB/EZ/commit/44ea55382f4d4eba90562dd4133c84bc697d34fa))
* suppress W2010 warning when nil-check is present ([#1077](https://github.com/SchoolyB/EZ/issues/1077)) ([82789fb](https://github.com/SchoolyB/EZ/commit/82789fb05c740832bd3029da0ea9b704cdc93683))

## [1.4.4](https://github.com/SchoolyB/EZ/compare/v1.4.3...v1.4.4) (2026-01-28)


### Bug Fixes

* code quality improvements and performance optimizations ([99523bf](https://github.com/SchoolyB/EZ/commit/99523bf016efdf07b9c85d34e918729631547b87))


### Performance Improvements

* optimize hot paths and eliminate code duplication ([e88ad38](https://github.com/SchoolyB/EZ/commit/e88ad38ea3405ed24c8745c347e9d84557c3f79c))
* optimize parser, tokenizer, errors, lineeditor, and db packages ([a52c4b6](https://github.com/SchoolyB/EZ/commit/a52c4b63a47c63fc9c8e4dc20690603ebf7374f8))

## [1.4.3](https://github.com/SchoolyB/EZ/compare/v1.4.2...v1.4.3) (2026-01-25)


### Bug Fixes

* apply bug fixes from recent PRs ([979d5e3](https://github.com/SchoolyB/EZ/commit/979d5e32c7e3d70883ade6a054a4eee29686c8d5))

## [1.4.2](https://github.com/SchoolyB/EZ/compare/v1.4.1...v1.4.2) (2026-01-24)


### Bug Fixes

* **typechecker:** resolve multi-return type inference for stdlib calls via 'using' ([#1062](https://github.com/SchoolyB/EZ/issues/1062)) ([0c21737](https://github.com/SchoolyB/EZ/commit/0c21737f4e3a6b0181aa5d87b330623c7675f0af)), closes [#977](https://github.com/SchoolyB/EZ/issues/977)

## [1.4.1](https://github.com/SchoolyB/EZ/compare/v1.4.0...v1.4.1) (2026-01-23)


### Bug Fixes

* **typechecker:** add E3041 check for global fixed-size array overflow ([#1060](https://github.com/SchoolyB/EZ/issues/1060)) ([56de4f1](https://github.com/SchoolyB/EZ/commit/56de4f1657d2d7bd53187854a39584e08b2640f3)), closes [#1058](https://github.com/SchoolyB/EZ/issues/1058)

## [1.4.0](https://github.com/SchoolyB/EZ/compare/v1.3.0...v1.4.0) (2026-01-22)


### Features

* **operators:** add map support for in/not_in operators ([#1053](https://github.com/SchoolyB/EZ/issues/1053)) ([4239d20](https://github.com/SchoolyB/EZ/commit/4239d2043a45ed65fede9d1c858aa2f98030687e)), closes [#1007](https://github.com/SchoolyB/EZ/issues/1007)


### Bug Fixes

* **parser:** allow nil as function return type ([#1054](https://github.com/SchoolyB/EZ/issues/1054)) ([473b26e](https://github.com/SchoolyB/EZ/commit/473b26eadffe4c2d5d287757b6832a83a8e79989)), closes [#1044](https://github.com/SchoolyB/EZ/issues/1044)
* **stdlib/math:** preserve precision for add, sub, mul, mod ([45ab8c4](https://github.com/SchoolyB/EZ/commit/45ab8c45337df3554acdc5d91f3b7bf52cd15f9c))
* **stdlib/math:** preserve precision for factorial, gcd, lcm ([d7dc223](https://github.com/SchoolyB/EZ/commit/d7dc2232997223e678a36b28e26dab85f3d2ceed))
* **stdlib/math:** preserve precision for large integers ([88187fb](https://github.com/SchoolyB/EZ/commit/88187fb3c4662b83a8cd6944b977223e86e6ca51))
* **stdlib/math:** preserve precision for min, max, clamp ([b9ba598](https://github.com/SchoolyB/EZ/commit/b9ba5989d851cb63a831e0f74284b352147c3dfe))
* **stdlib/math:** preserve precision for pow, sum ([e6eada0](https://github.com/SchoolyB/EZ/commit/e6eada0a6f9fc6481dfccdc9126ea5a2cf1b8788))
* **stdlib/math:** preserve precision for sign ([c7ba2f1](https://github.com/SchoolyB/EZ/commit/c7ba2f18b69049bdb438f5b30f7927662388f2ec))
* **tests:** remove E17004_db_corrupted test ([#1052](https://github.com/SchoolyB/EZ/issues/1052)) ([275bdb3](https://github.com/SchoolyB/EZ/commit/275bdb352388c5b911cb15e310e6960985b44341)), closes [#1051](https://github.com/SchoolyB/EZ/issues/1051)

## [1.3.0](https://github.com/SchoolyB/EZ/compare/v1.2.0...v1.3.0) (2026-01-19)


### Features

* **stdlib:** Add Unix timestamp functions and date utilities to time module ([#1023](https://github.com/SchoolyB/EZ/issues/1023)) ([#1043](https://github.com/SchoolyB/EZ/issues/1043)) ([bdb24e8](https://github.com/SchoolyB/EZ/commit/bdb24e8bd29ca113ed294330e9eae4c4ad1dc08e))

## [1.2.0](https://github.com/SchoolyB/EZ/compare/v1.1.0...v1.2.0) (2026-01-19)


### Features

* **lexer:** add \x hex escape sequence support in strings and chars ([#1046](https://github.com/SchoolyB/EZ/issues/1046)) ([3d4eae7](https://github.com/SchoolyB/EZ/commit/3d4eae7764ab4f53c3488357aa70b55dae877674)), closes [#1045](https://github.com/SchoolyB/EZ/issues/1045)

## [1.1.0](https://github.com/SchoolyB/EZ/compare/v1.0.2...v1.1.0) (2026-01-18)


### Features

* stdlib enhancements, bug fixes, and type system improvements ([2362596](https://github.com/SchoolyB/EZ/commit/2362596910747cccbe7ba80726aa038a22aff045))
* **stdlib:** add `db.entries()` function ([#1035](https://github.com/SchoolyB/EZ/issues/1035)) ([093742f](https://github.com/SchoolyB/EZ/commit/093742fed2fe3b99a23ba78a02e20b39f08be6e4)), closes [#1025](https://github.com/SchoolyB/EZ/issues/1025)
* **stdlib:** add arrays.equals() function ([#1033](https://github.com/SchoolyB/EZ/issues/1033)) ([67258bd](https://github.com/SchoolyB/EZ/commit/67258bd0ebf7352f711f94d4254fa72e2701fadf)), closes [#964](https://github.com/SchoolyB/EZ/issues/964)
* **stdlib:** add db.values() function ([#1032](https://github.com/SchoolyB/EZ/issues/1032)) ([3dd7dd0](https://github.com/SchoolyB/EZ/commit/3dd7dd02a828fbafbe23412a6cdb9f5090d8450e)), closes [#943](https://github.com/SchoolyB/EZ/issues/943)
* **stdlib:** add http.head, options, download, parse_url, build_url ([#1034](https://github.com/SchoolyB/EZ/issues/1034)) ([e89b899](https://github.com/SchoolyB/EZ/commit/e89b8998304898e4f5d5ff93e58d3b0f8f6aeb2a)), closes [#1022](https://github.com/SchoolyB/EZ/issues/1022)


### Bug Fixes

* context-aware return type inference for array literals ([#1008](https://github.com/SchoolyB/EZ/issues/1008)) ([31ed9fa](https://github.com/SchoolyB/EZ/commit/31ed9fa5a077345c569e581952479d98566d6f82))
* **interpreter:** context-aware return type inference for array literals ([1353cc1](https://github.com/SchoolyB/EZ/commit/1353cc181743ac6a76b45b56fd682efa29277584)), closes [#1008](https://github.com/SchoolyB/EZ/issues/1008)
* **interpreter:** infer element type for array literals ([45a18dc](https://github.com/SchoolyB/EZ/commit/45a18dc664aa554784f84a57d9015b4f146f1f01)), closes [#1008](https://github.com/SchoolyB/EZ/issues/1008)
* **typechecker:** context-aware return type validation for array literals ([2920d77](https://github.com/SchoolyB/EZ/commit/2920d77425da7e56c59410bfb32a9a32bef99a48))
* **typechecker:** recognize when/default as exhaustive return coverage ([9db5c52](https://github.com/SchoolyB/EZ/commit/9db5c521acb273b5f328032f72264eb1fe9d21b1))
* **typechecker:** recognize when/default as exhaustive return coverage ([978a4d1](https://github.com/SchoolyB/EZ/commit/978a4d1fda24199f9e43775798ebf801b396e337)), closes [#918](https://github.com/SchoolyB/EZ/issues/918)

## [1.0.2](https://github.com/SchoolyB/EZ/compare/v1.0.1...v1.0.2) (2026-01-17)


### Bug Fixes

* **typechecker:** error when fixed-size array has too many elements ([#1030](https://github.com/SchoolyB/EZ/issues/1030)) ([7d09424](https://github.com/SchoolyB/EZ/commit/7d09424f2bd6128e624a772b8ce2165b15b98c7e)), closes [#1029](https://github.com/SchoolyB/EZ/issues/1029)

## [1.0.1](https://github.com/SchoolyB/EZ/compare/v1.0.0...v1.0.1) (2026-01-15)


### Bug Fixes

* **interpreter:** add error codes and location info to runtime errors ([#1009](https://github.com/SchoolyB/EZ/issues/1009)) ([#1013](https://github.com/SchoolyB/EZ/issues/1013)) ([d1bb289](https://github.com/SchoolyB/EZ/commit/d1bb2897768307a194bbe71b5df8574b976ba272))
* **interpreter:** add range checking for integer type narrowing ([#962](https://github.com/SchoolyB/EZ/issues/962)) ([#1016](https://github.com/SchoolyB/EZ/issues/1016)) ([02f953b](https://github.com/SchoolyB/EZ/commit/02f953bb6e4efb2b42c47af5708ac5826abd5723))
* **stdlib:** handle empty database files in db.open() ([#941](https://github.com/SchoolyB/EZ/issues/941)) ([#1012](https://github.com/SchoolyB/EZ/issues/1012)) ([eadc48d](https://github.com/SchoolyB/EZ/commit/eadc48d3edb7817aeddf8b405b01697d6015b3ff))
* **stdlib:** improve error message when db file contains JSON array ([#942](https://github.com/SchoolyB/EZ/issues/942)) ([#1014](https://github.com/SchoolyB/EZ/issues/1014)) ([bea2f65](https://github.com/SchoolyB/EZ/commit/bea2f659dd141a09014e4a3d7fefd31796380050))
* **typechecker:** use correct error code E5010 for continue outside loop ([#963](https://github.com/SchoolyB/EZ/issues/963)) ([#1011](https://github.com/SchoolyB/EZ/issues/1011)) ([9f55570](https://github.com/SchoolyB/EZ/commit/9f55570b34c66af16e7eb46cc630801361fe6e87))

## [1.0.0](https://github.com/SchoolyB/EZ/compare/v0.40.5...v1.0.0) (2026-01-14)


### ⚠ BREAKING CHANGES

* Existing code using removed/renamed functions must be updated.

### Features

* **#996:** Rename stdlib functions for consistency ([#1001](https://github.com/SchoolyB/EZ/issues/1001)) ([0ad96f8](https://github.com/SchoolyB/EZ/commit/0ad96f881a24123d6fba7f414a48bdb0b819a22d))
* stdlib function renaming for consistency ([09b658b](https://github.com/SchoolyB/EZ/commit/09b658b681593511294c6fe41d762d117c2aea4f))


### Code Refactoring

* remove duplicate stdlib aliases and rename db functions ([#1003](https://github.com/SchoolyB/EZ/issues/1003)) ([4e0dc08](https://github.com/SchoolyB/EZ/commit/4e0dc081711bd70b237bd71fde809972b0db7eca)), closes [#995](https://github.com/SchoolyB/EZ/issues/995) [#997](https://github.com/SchoolyB/EZ/issues/997)

## [0.40.5](https://github.com/SchoolyB/EZ/compare/v0.40.4...v0.40.5) (2026-01-11)


### Bug Fixes

* Add `isMultiReturnCall` to typechecker ([#951](https://github.com/SchoolyB/EZ/issues/951)) ([981d068](https://github.com/SchoolyB/EZ/commit/981d068676520c1bd1a545c8f0b524ff614856eb))
* **cli:** Allow command line arguments for programs ([#983](https://github.com/SchoolyB/EZ/issues/983)) ([9f4439d](https://github.com/SchoolyB/EZ/commit/9f4439d29be136c720d62d2c3bb0f971e60a414e))
* Detect invalid string interpolation syntax at parse time ([#988](https://github.com/SchoolyB/EZ/issues/988)) ([7fcbcc1](https://github.com/SchoolyB/EZ/commit/7fcbcc152400e7b8e201eef2c92153a1d56c488d)), closes [#984](https://github.com/SchoolyB/EZ/issues/984)
* Error on bare function/type names as statements ([#989](https://github.com/SchoolyB/EZ/issues/989)) ([a84ab6b](https://github.com/SchoolyB/EZ/commit/a84ab6b2c742b5411ce84da4b54ff0785549c24a)), closes [#985](https://github.com/SchoolyB/EZ/issues/985)
* Prevent RETURN_VALUE type leak for multi-return functions ([#987](https://github.com/SchoolyB/EZ/issues/987)) ([750906f](https://github.com/SchoolyB/EZ/commit/750906fcbb445ecdf119c0a8f9204453674a2dcf)), closes [#986](https://github.com/SchoolyB/EZ/issues/986)

## [0.40.4](https://github.com/SchoolyB/EZ/compare/v0.40.3...v0.40.4) (2026-01-10)


### Bug Fixes

* resolve integration test failures on Linux ([#981](https://github.com/SchoolyB/EZ/issues/981)) ([b20d676](https://github.com/SchoolyB/EZ/commit/b20d676e28d3dff80ab408a3f6ec698f43918b0f)), closes [#978](https://github.com/SchoolyB/EZ/issues/978)

## [0.40.3](https://github.com/SchoolyB/EZ/compare/v0.40.2...v0.40.3) (2026-01-10)


### Bug Fixes

* Typechecker modification to resolve "using directive" bug ([#979](https://github.com/SchoolyB/EZ/issues/979)) ([42cf234](https://github.com/SchoolyB/EZ/commit/42cf23451c47dc40211e8d636f6abae56f4eb3a4))

## [0.40.2](https://github.com/SchoolyB/EZ/compare/v0.40.1...v0.40.2) (2026-01-10)


### Bug Fixes

* **ci:** use EZ_DOCS_SYNC token for website repo access ([#974](https://github.com/SchoolyB/EZ/issues/974)) ([f47c649](https://github.com/SchoolyB/EZ/commit/f47c649a5f6bf012e315fc7a5f414fae0180641d))

## [0.40.1](https://github.com/SchoolyB/EZ/compare/v0.40.0...v0.40.1) (2026-01-10)


### Bug Fixes

* **ci:** create wasm directory before copying files ([#972](https://github.com/SchoolyB/EZ/issues/972)) ([193ddcb](https://github.com/SchoolyB/EZ/commit/193ddcb8fd461eb8a599d8b84e4e3a2603401899))

## [0.40.0](https://github.com/SchoolyB/EZ/compare/v0.39.3...v0.40.0) (2026-01-10)


### Features

* **wasm:** add WebAssembly build for browser playground ([#970](https://github.com/SchoolyB/EZ/issues/970)) ([89e860e](https://github.com/SchoolyB/EZ/commit/89e860e4c41865fe1e0a82e9a26ea64d8913b10e))

## [0.39.3](https://github.com/SchoolyB/EZ/compare/v0.39.2...v0.39.3) (2026-01-09)


### Bug Fixes

* **interpreter,stdlib:** replace .Type() with helper functions in error messages ([#956](https://github.com/SchoolyB/EZ/issues/956)) ([61cc075](https://github.com/SchoolyB/EZ/commit/61cc07522f3d5870320a2fd9141fe504a74fe62a)), closes [#948](https://github.com/SchoolyB/EZ/issues/948)
* **interpreter:** add Map case to objectTypeToEZ function ([#955](https://github.com/SchoolyB/EZ/issues/955)) ([8ac5396](https://github.com/SchoolyB/EZ/commit/8ac53962ac63ac22a666ccc77ab4f42be59a0f8a)), closes [#945](https://github.com/SchoolyB/EZ/issues/945)
* **interpreter:** update type name functions with missing types ([#946](https://github.com/SchoolyB/EZ/issues/946)) ([#958](https://github.com/SchoolyB/EZ/issues/958)) ([0774dde](https://github.com/SchoolyB/EZ/commit/0774dde15d73cbbda2fb516915f47c648421f09f))
* **lexer,parser:** add explicit 0o octal prefix, treat leading zeros as decimal ([#954](https://github.com/SchoolyB/EZ/issues/954)) ([b8e7f41](https://github.com/SchoolyB/EZ/commit/b8e7f418b4575480a95afb46501a68c5d1136fde)), closes [#915](https://github.com/SchoolyB/EZ/issues/915)
* **repl:** prevent E4001 error when running REPL commands ([#953](https://github.com/SchoolyB/EZ/issues/953)) ([019a81b](https://github.com/SchoolyB/EZ/commit/019a81befa384bb086868b23f6f767a2eb83ca4b)), closes [#890](https://github.com/SchoolyB/EZ/issues/890)
* **typechecker,stdlib,tests:** fix integration test failures ([#952](https://github.com/SchoolyB/EZ/issues/952)) ([#960](https://github.com/SchoolyB/EZ/issues/960)) ([f528389](https://github.com/SchoolyB/EZ/commit/f528389001fb1e291417c6439dc0ecda04b56a6c))
* **typechecker:** require type argument for json.decode ([#947](https://github.com/SchoolyB/EZ/issues/947)) ([#957](https://github.com/SchoolyB/EZ/issues/957)) ([2cbb2c2](https://github.com/SchoolyB/EZ/commit/2cbb2c21375eba690b7a807685afb0f8a4dda9c8))

## [0.39.2](https://github.com/SchoolyB/EZ/compare/v0.39.1...v0.39.2) (2026-01-07)


### Bug Fixes

* **interpreter:** allow arbitrary precision arithmetic for int/uint types ([#917](https://github.com/SchoolyB/EZ/issues/917)) ([#931](https://github.com/SchoolyB/EZ/issues/931)) ([728cd19](https://github.com/SchoolyB/EZ/commit/728cd195b90ddbf3cf373814e6765e2205f0b763))
* **parser:** error on invalid operators in string interpolation ([#916](https://github.com/SchoolyB/EZ/issues/916)) ([#933](https://github.com/SchoolyB/EZ/issues/933)) ([54b03bc](https://github.com/SchoolyB/EZ/commit/54b03bcdfed35e0b54bd7dec2262f0f199cf8a04))
* **typechecker:** show correct error for invalid sized types with using directive ([#914](https://github.com/SchoolyB/EZ/issues/914)) ([#932](https://github.com/SchoolyB/EZ/issues/932)) ([9ba4bc0](https://github.com/SchoolyB/EZ/commit/9ba4bc0217edabee4504bac0feca8a8f8b76e3e6))

## [0.39.1](https://github.com/SchoolyB/EZ/compare/v0.39.0...v0.39.1) (2026-01-06)


### Bug Fixes

* **update:** exit original process after sudo completes ([#927](https://github.com/SchoolyB/EZ/issues/927)) ([266c5c3](https://github.com/SchoolyB/EZ/commit/266c5c3f759067db37e6043b62e5d60a8bfc5468))

## [0.39.0](https://github.com/SchoolyB/EZ/compare/v0.38.0...v0.39.0) (2026-01-06)


### Features

* **time:** add weekday, month and duration constants (resolves [#902](https://github.com/SchoolyB/EZ/issues/902)) ([#923](https://github.com/SchoolyB/EZ/issues/923)) ([179fe62](https://github.com/SchoolyB/EZ/commit/179fe6290e8e95b35085387a2969f911bd87067b))

## [0.38.0](https://github.com/SchoolyB/EZ/compare/v0.37.0...v0.38.0) (2026-01-06)


### Features

* **cli:** improve ez update changelog display ([#920](https://github.com/SchoolyB/EZ/issues/920)) ([7125b83](https://github.com/SchoolyB/EZ/commit/7125b83f4df95183c25795722fd95086f6f3ca3d)), closes [#919](https://github.com/SchoolyB/EZ/issues/919)

## [0.37.0](https://github.com/SchoolyB/EZ/compare/v0.36.7...v0.37.0) (2026-01-05)


### Features

* **http:** add HTTP status code constants ([#907](https://github.com/SchoolyB/EZ/issues/907)) ([5ce155d](https://github.com/SchoolyB/EZ/commit/5ce155d7163d83a3f6bd68ba5e3be618de58b4ac))

## [0.36.7](https://github.com/SchoolyB/EZ/compare/v0.36.6...v0.36.7) (2026-01-04)


### Bug Fixes

* **ci:** use file -b to avoid matching on filenames in sanity check ([f01ca70](https://github.com/SchoolyB/EZ/commit/f01ca70345368e389e7d9880e0ab4111be557e26))
* Internal type representation leaks Go type names instead of EZ types ([26dd6c1](https://github.com/SchoolyB/EZ/commit/26dd6c12921edf797e93ecc68b08be9b7d2048cd))
* **interpreter:** set Map KeyType/ValueType when maps are created ([04e164f](https://github.com/SchoolyB/EZ/commit/04e164fc6932f5929f3f877aa7a13245e0930c66))
* **stdlib:** add DeclaredType to float decode functions in binary module ([2fd5582](https://github.com/SchoolyB/EZ/commit/2fd558242534d5185e2b84a5eba5e8f8958f978a))
* **stdlib:** add ElementType to bytes.split outer array ([330cb1d](https://github.com/SchoolyB/EZ/commit/330cb1db88060fd7a358523ee5adb6cd77ec9aac))
* **stdlib:** add ElementType to empty array in crypto.random_bytes ([02293e1](https://github.com/SchoolyB/EZ/commit/02293e197ac63c8af5a42740a8fe0090b725152d))
* **stdlib:** preserve ElementType in arrays module functions ([bb0f8de](https://github.com/SchoolyB/EZ/commit/bb0f8dec4f1b084682e1334f1fad9dd6fc98c816)), closes [#900](https://github.com/SchoolyB/EZ/issues/900)
* **stdlib:** preserve type info in `[@maps](https://github.com/maps)` module and copyByDefault ([5a0259a](https://github.com/SchoolyB/EZ/commit/5a0259a430b2c5a0df65e926f78b6b2c938f42c0))
* **stdlib:** preserve type info in builtins and `[@strings](https://github.com/strings)` modules ([0dc4d44](https://github.com/SchoolyB/EZ/commit/0dc4d44efb1fa9ea29a593fa6d5829e59f075aa3))
* **stdlib:** set DeclaredType for floats in json module ([cb0d46f](https://github.com/SchoolyB/EZ/commit/cb0d46f6c1d5d1065955f66b965bd0644ecbbed8)), closes [#900](https://github.com/SchoolyB/EZ/issues/900)
* **stdlib:** set ElementType for arrays in db module ([6e5086a](https://github.com/SchoolyB/EZ/commit/6e5086a4b9e6c524267fde59ea40a150d0b6e6b5)), closes [#900](https://github.com/SchoolyB/EZ/issues/900)
* **stdlib:** set ElementType for arrays in io module ([637bbb7](https://github.com/SchoolyB/EZ/commit/637bbb7812b7eb1430824a12efb69ec8757fb7df)), closes [#900](https://github.com/SchoolyB/EZ/issues/900)
* **stdlib:** set proper types for headers map and arrays in http module ([450c5f3](https://github.com/SchoolyB/EZ/commit/450c5f3b7be43b4d3c3b84c1673d5b7942005371))
* **stdlib:** set proper types in os module ([bba1458](https://github.com/SchoolyB/EZ/commit/bba1458f8bee9531162a3704e7c0a6b977456db2)), closes [#900](https://github.com/SchoolyB/EZ/issues/900)
* **stdlib:** set proper types in random module ([4739f16](https://github.com/SchoolyB/EZ/commit/4739f161aa6872b4f0485bd7bd72ac953cc45499)), closes [#900](https://github.com/SchoolyB/EZ/issues/900)
* **stdlib:** update getEZTypeName to return proper EZ type names ([d8ee463](https://github.com/SchoolyB/EZ/commit/d8ee463a969c1043062f53ee4a0322ad9ad29b72))
* **typechecker:** reject typeof() on void function results ([ff9897d](https://github.com/SchoolyB/EZ/commit/ff9897d233e0b3f2ccefdd52412bd8b317552ff1))
* **types:** add DeclaredType support for Float and sized type conversions ([979e9fd](https://github.com/SchoolyB/EZ/commit/979e9fdd28dcea79f43539b6a1eda35d959b71fe))
* **types:** typeof() returns "Database" for database objects ([ad2ed95](https://github.com/SchoolyB/EZ/commit/ad2ed951b639438040c8a9f9711114403d3e0486)), closes [#900](https://github.com/SchoolyB/EZ/issues/900)
* **types:** typeof() returns "Range&lt;int&gt;" for range objects ([64cbb0a](https://github.com/SchoolyB/EZ/commit/64cbb0a762a032e370a41b7fb1cc6f5e952aa367)), closes [#900](https://github.com/SchoolyB/EZ/issues/900)
* **types:** typeof() returns Ref&lt;innerType&gt; for references ([8b06b9b](https://github.com/SchoolyB/EZ/commit/8b06b9b906d5c8f6589fbd95e47f2bb4bf75a991)), closes [#900](https://github.com/SchoolyB/EZ/issues/900)
* **types:** use "File" as user-facing type name for FileHandle ([c4d9a5a](https://github.com/SchoolyB/EZ/commit/c4d9a5abaac754c7c39d7a8117489cad0281f590)), closes [#900](https://github.com/SchoolyB/EZ/issues/900)

## [0.36.6](https://github.com/SchoolyB/EZ/compare/v0.36.5...v0.36.6) (2026-01-04)


### Bug Fixes

* **errors:** update E3038 hint to be more accurate ([a34b1b5](https://github.com/SchoolyB/EZ/commit/a34b1b5a42edcfd453c5562c5c2c3df9936a9fa2))
* **interpreter:** handle void return with ensure correctly ([5580b07](https://github.com/SchoolyB/EZ/commit/5580b0777818975cda78a27be53baee1ec72320f)), closes [#883](https://github.com/SchoolyB/EZ/issues/883)
* **typechecker:** prevent assignment of void function results ([a574be5](https://github.com/SchoolyB/EZ/commit/a574be5a5888e1dcd6d46bd0b043a67438b3323d))
* **typechecker:** reject void as explicit return type ([d307711](https://github.com/SchoolyB/EZ/commit/d307711471dcbd5872c6f5f2274ec337d859e89a))
* **typechecker:** reject void in compound types ([b2182bf](https://github.com/SchoolyB/EZ/commit/b2182bfaac444ef37a47c643cdcf591102a7eb85))
* void function fixes and comprehensive type rejection ([e504704](https://github.com/SchoolyB/EZ/commit/e504704238c91dd7ab4e8f65476412160aed4e10))

## [0.36.5](https://github.com/SchoolyB/EZ/compare/v0.36.4...v0.36.5) (2026-01-04)


### Bug Fixes

* **repl:** add multi-line navigation support ([33381b0](https://github.com/SchoolyB/EZ/commit/33381b0de8b973edf8cad6424f1ae86771c6b0b2))
* **repl:** add multi-line navigation support ([a4dcf3d](https://github.com/SchoolyB/EZ/commit/a4dcf3dacb11dc072574a9a7c0de3c368bdeb93c)), closes [#875](https://github.com/SchoolyB/EZ/issues/875)

## [0.36.4](https://github.com/SchoolyB/EZ/compare/v0.36.3...v0.36.4) (2026-01-03)


### Bug Fixes

* **typechecker:** runtime string relational operator failure ([#888](https://github.com/SchoolyB/EZ/issues/888)) ([bc7aee4](https://github.com/SchoolyB/EZ/commit/bc7aee4cdb23dc89e05b7ee84156cf3ee8d92137))

## [0.36.3](https://github.com/SchoolyB/EZ/compare/v0.36.2...v0.36.3) (2025-12-31)


### Features

* add`[@http](https://github.com/http)` module HTTP client for web requests ([#877](https://github.com/SchoolyB/EZ/issues/877)) ([34a874f](https://github.com/SchoolyB/EZ/commit/34a874f753f68ff8fbd52ea83a9ff179dad3b2fd))


### Bug Fixes

* Bug: Type inference fails for most stdlib module function calls ([#878](https://github.com/SchoolyB/EZ/issues/878)) ([4b6bfa7](https://github.com/SchoolyB/EZ/commit/4b6bfa79c95250241da3f127230ea33317e4f037))
* resolve merge conflict and regenerate ERRORS.md ([53cc4da](https://github.com/SchoolyB/EZ/commit/53cc4da6f34cc3f644f19d022e5e06a6279a5cf8))
* **typechecker:** infer json.decode return type from type argument ([908b026](https://github.com/SchoolyB/EZ/commit/908b0265b1df41b75c39cd75679ee13282ab7c14))

## [0.36.2](https://github.com/SchoolyB/EZ/compare/v0.36.1...v0.36.2) (2025-12-28)


### Bug Fixes

* **ensure:** add missing validations and revert workflow change ([#866](https://github.com/SchoolyB/EZ/issues/866)) ([e502fbd](https://github.com/SchoolyB/EZ/commit/e502fbd2e41abf074ddff95ef71f6b1ab91373a0))

## [0.36.1](https://github.com/SchoolyB/EZ/compare/v0.36.0...v0.36.1) (2025-12-28)


### Features

* `ensure` keyword for guaranteed cleanup on function exit [#804](https://github.com/SchoolyB/EZ/issues/804) ([#864](https://github.com/SchoolyB/EZ/issues/864)) ([cbef798](https://github.com/SchoolyB/EZ/commit/cbef7983e727a194b4453fc38e48e83ac2fb319a))

## [0.36.0](https://github.com/SchoolyB/EZ/compare/v0.35.0...v0.36.0) (2025-12-28)


### Features

* stdlib additions and bug fixes ([88791f4](https://github.com/SchoolyB/EZ/commit/88791f4a39b32b68365b5f50e977f763839d9a96))
* **stdlib:** add [@crypto](https://github.com/crypto) module for hashing and secure random ([9a38974](https://github.com/SchoolyB/EZ/commit/9a3897430d77b6561d6dee76c34e50fcdf5f317d)), closes [#458](https://github.com/SchoolyB/EZ/issues/458)
* **stdlib:** add [@encoding](https://github.com/encoding) module with base64, hex, and URL functions ([58cf8b6](https://github.com/SchoolyB/EZ/commit/58cf8b6301769e58d323816bff6fe794ff6f55b6))
* **stdlib:** add [@uuid](https://github.com/uuid) module for UUID generation ([e283602](https://github.com/SchoolyB/EZ/commit/e283602315cffdf0f46635b55baf1fcff8bdf38a)), closes [#759](https://github.com/SchoolyB/EZ/issues/759)


### Bug Fixes

* **evaluator:** allow modifying nested struct fields in array elements ([4d5de68](https://github.com/SchoolyB/EZ/commit/4d5de68500fb29a6d00d729ce141704377c22df2)), closes [#859](https://github.com/SchoolyB/EZ/issues/859)
* **evaluator:** prevent stack overflow on self-referential structs ([6f68d98](https://github.com/SchoolyB/EZ/commit/6f68d981901738e4b6a6d880e61a9650cbe971a8)), closes [#860](https://github.com/SchoolyB/EZ/issues/860)
* **parser:** allow blank identifier _ in for and for_each loops ([456e75d](https://github.com/SchoolyB/EZ/commit/456e75dcdc287b762fa505561bfe8790c1f03295)), closes [#858](https://github.com/SchoolyB/EZ/issues/858)
* **typechecker:** allow int/float comparison with == and != operators ([0a5b97d](https://github.com/SchoolyB/EZ/commit/0a5b97d90dbc0b94544f03567190aa3d8c9ce39f)), closes [#857](https://github.com/SchoolyB/EZ/issues/857)

## [0.35.0](https://github.com/SchoolyB/EZ/compare/v0.34.1...v0.35.0) (2025-12-27)


### Features

* ASCII art banner ([#855](https://github.com/SchoolyB/EZ/issues/855)) ([4ccaea8](https://github.com/SchoolyB/EZ/commit/4ccaea8989729e55beb068cc0ee0cd5aec8389f8))

## [0.34.1](https://github.com/SchoolyB/EZ/compare/v0.34.0...v0.34.1) (2025-12-27)


### Bug Fixes

* **typechecker:** resolve struct parameter member access for imported types ([#851](https://github.com/SchoolyB/EZ/issues/851)) ([#853](https://github.com/SchoolyB/EZ/issues/853)) ([dada274](https://github.com/SchoolyB/EZ/commit/dada2740cca72f88d8ed56699d7596e38e368bfe))

## [0.34.0](https://github.com/SchoolyB/EZ/compare/v0.33.4...v0.34.0) (2025-12-26)


### Features

* add warning for unused imports ([#639](https://github.com/SchoolyB/EZ/issues/639)) ([#844](https://github.com/SchoolyB/EZ/issues/844)) ([d299bcd](https://github.com/SchoolyB/EZ/commit/d299bcdcbc750037d68ceb591c94c951abcf1152))
* **examples:** add price calculator example ([#848](https://github.com/SchoolyB/EZ/issues/848)) ([70d10b7](https://github.com/SchoolyB/EZ/commit/70d10b721970f2fb266c892128b974ad9d069f15))


### Bug Fixes

* **examples:** resolve W2009 warning in json.ez ([#357](https://github.com/SchoolyB/EZ/issues/357)) ([#847](https://github.com/SchoolyB/EZ/issues/847)) ([20815bb](https://github.com/SchoolyB/EZ/commit/20815bb81d24c2c4803d89e0c65daf162941f032))

## [0.33.4](https://github.com/SchoolyB/EZ/compare/v0.33.3...v0.33.4) (2025-12-26)


### Bug Fixes

* UTF-8 characters corrupted in interpolated strings ([#839](https://github.com/SchoolyB/EZ/issues/839)) ([ebb34dc](https://github.com/SchoolyB/EZ/commit/ebb34dc145235f85d7fbb3dc748132fd10a0e4bf))

## [0.33.3](https://github.com/SchoolyB/EZ/compare/v0.33.2...v0.33.3) (2025-12-25)


### Bug Fixes

* type inference for user module functions and void type validation ([#837](https://github.com/SchoolyB/EZ/issues/837)) ([c63c48f](https://github.com/SchoolyB/EZ/commit/c63c48f5d9e1cfad52c914e1f018e3e75e0621e6))

## [0.33.2](https://github.com/SchoolyB/EZ/compare/v0.33.1...v0.33.2) (2025-12-25)


### Bug Fixes

* #suppress before function now correctly applies to function only ([#830](https://github.com/SchoolyB/EZ/issues/830), [#831](https://github.com/SchoolyB/EZ/issues/831)) ([#832](https://github.com/SchoolyB/EZ/issues/832)) ([6837668](https://github.com/SchoolyB/EZ/commit/68376685eab9e4aeec51b5b3454aac704a90b34c))
* add cleanup for database test files ([#800](https://github.com/SchoolyB/EZ/issues/800)) ([#829](https://github.com/SchoolyB/EZ/issues/829)) ([35cfec8](https://github.com/SchoolyB/EZ/commit/35cfec8bcadb9bae1b7d1bc14f551a903473804f))
* add overflow and division-by-zero checks for float arithmetic ([#798](https://github.com/SchoolyB/EZ/issues/798)) ([#826](https://github.com/SchoolyB/EZ/issues/826)) ([476c18d](https://github.com/SchoolyB/EZ/commit/476c18d284d5841972a248701c6f3e22236d9196))
* add overflow/underflow checks for byte arithmetic ([#817](https://github.com/SchoolyB/EZ/issues/817)) ([#822](https://github.com/SchoolyB/EZ/issues/822)) ([5bd37ba](https://github.com/SchoolyB/EZ/commit/5bd37ba8ab7e2d538d27cf163e9f7822c2e38170))
* disallow loop variable shadowing ([#114](https://github.com/SchoolyB/EZ/issues/114)) ([#835](https://github.com/SchoolyB/EZ/issues/835)) ([1cd45c2](https://github.com/SchoolyB/EZ/commit/1cd45c272113f1473b27e4d5c3557c1892817eee))
* make arrays.remove_all() consistent with other remove functions ([#820](https://github.com/SchoolyB/EZ/issues/820)) ([#825](https://github.com/SchoolyB/EZ/issues/825)) ([725d34d](https://github.com/SchoolyB/EZ/commit/725d34dd10dc86c7d2f1bdac44af712e90c1b3fb))
* os.exec now returns error on non-zero exit code ([#799](https://github.com/SchoolyB/EZ/issues/799)) ([#827](https://github.com/SchoolyB/EZ/issues/827)) ([06ee450](https://github.com/SchoolyB/EZ/commit/06ee450ed261fad68b87d0b8ee0d420eeb5b6220))
* prevent json.encode() from overwriting EncodeAsString conversion ([#818](https://github.com/SchoolyB/EZ/issues/818)) ([#823](https://github.com/SchoolyB/EZ/issues/823)) ([85544e7](https://github.com/SchoolyB/EZ/commit/85544e7e70499baba4814579564d8690d1f89f94))
* prevent panic on multi-return type mismatch with fewer names than types ([#816](https://github.com/SchoolyB/EZ/issues/816)) ([#821](https://github.com/SchoolyB/EZ/issues/821)) ([d983679](https://github.com/SchoolyB/EZ/commit/d98367975d9be03db6b95e5e8ab4171f164be36c))
* properly extract first rune in strings.from_chars() ([#819](https://github.com/SchoolyB/EZ/issues/819)) ([#824](https://github.com/SchoolyB/EZ/issues/824)) ([060cfa6](https://github.com/SchoolyB/EZ/commit/060cfa67b746b3ff22944a584fde367c26ce4fc2))

## [0.33.1](https://github.com/SchoolyB/EZ/compare/v0.33.0...v0.33.1) (2025-12-24)


### Bug Fixes

* mutable parameters now work with indexed/member expressions ([#813](https://github.com/SchoolyB/EZ/issues/813)) ([4b7bdf2](https://github.com/SchoolyB/EZ/commit/4b7bdf2cfd961e8623d025066d2875ddc472fcc9)), closes [#797](https://github.com/SchoolyB/EZ/issues/797)
* prevent array mutation during for_each iteration ([#812](https://github.com/SchoolyB/EZ/issues/812)) ([00e0c83](https://github.com/SchoolyB/EZ/commit/00e0c8396b97c2753c5da05713cbaa627f25f7f5)), closes [#796](https://github.com/SchoolyB/EZ/issues/796)
* type inference for user-defined module function return types ([#811](https://github.com/SchoolyB/EZ/issues/811)) ([be278e7](https://github.com/SchoolyB/EZ/commit/be278e72ac1c59bf6675e688f1c13c9324ad6b56)), closes [#807](https://github.com/SchoolyB/EZ/issues/807)

## [0.33.0](https://github.com/SchoolyB/EZ/compare/v0.32.0...v0.33.0) (2025-12-23)


### Features

* add PowerShell install script for Windows ([e5ca88b](https://github.com/SchoolyB/EZ/commit/e5ca88bc7595be9beea852117c88d6c704cf3644))
* add PowerShell install script for Windows ([2244edb](https://github.com/SchoolyB/EZ/commit/2244edbb6c0b74f32e697710273ca459c1fc0a00)), closes [#806](https://github.com/SchoolyB/EZ/issues/806)

## [0.32.0](https://github.com/SchoolyB/EZ/compare/v0.31.0...v0.32.0) (2025-12-23)


### Features

* added workflow for checking PR validity based on filetype ([632d8bd](https://github.com/SchoolyB/EZ/commit/632d8bdf1b58fd9316ca5af5e2f13aed143168ff))


### Bug Fixes

* **ci:** add more file extension checks ([c6223fd](https://github.com/SchoolyB/EZ/commit/c6223fd8483db67bb6336dd6b84bf6391791d765))
* **ci:** correct workflow issues in PR sanity check ([9adafdd](https://github.com/SchoolyB/EZ/commit/9adafdd322c0b194c9fc6b20928d91f6a4280676))

## [0.31.0](https://github.com/SchoolyB/EZ/compare/v0.30.2...v0.31.0) (2025-12-22)


### Features

* **stdlib:** add db.exists() and db.update_key_name() ([f89aac1](https://github.com/SchoolyB/EZ/commit/f89aac142eb5344e7bc86a4500353a1d9cd2c74b))
* **stdlib:** add db.sort() with sort order constants ([8a26dab](https://github.com/SchoolyB/EZ/commit/8a26dab2c040d2372b004c97d71b9e15363794ed)), closes [#782](https://github.com/SchoolyB/EZ/issues/782)


### Bug Fixes

* **cli:** always fetch fresh version info for `ez version` command ([ffe4979](https://github.com/SchoolyB/EZ/commit/ffe49794dae0b9e5abd6189d5392c3ef9a45a5ec))
* **stdlib:** show overflow error instead of invalid format for large integers ([e4ff4bb](https://github.com/SchoolyB/EZ/commit/e4ff4bbbf01e9164aeb3199eb63dee919b78160a)), closes [#783](https://github.com/SchoolyB/EZ/issues/783)
* **tests:** strengthen db.ez assertions to actually verify behavior ([5e2bd65](https://github.com/SchoolyB/EZ/commit/5e2bd652f620db758e20f1ec3c69193bb3b32480))

## [0.30.2](https://github.com/SchoolyB/EZ/compare/v0.30.1...v0.30.2) (2025-12-22)


### Bug Fixes

* **typechecker:** require Database type for db module functions ([2d63dc6](https://github.com/SchoolyB/EZ/commit/2d63dc6b9b10582e26102023f9a31cd7497af976))
* **typechecker:** require Database type for db module functions ([851a6c2](https://github.com/SchoolyB/EZ/commit/851a6c2da1c824ef48c90f4af6c4a790695a2c87)), closes [#781](https://github.com/SchoolyB/EZ/issues/781)

## [0.30.1](https://github.com/SchoolyB/EZ/compare/v0.30.0...v0.30.1) (2025-12-22)


### Bug Fixes

* **stdlib:** write valid JSON when creating new database file ([ecb396a](https://github.com/SchoolyB/EZ/commit/ecb396a07e99e93519fcb3677e89b26fa66b9956))
* **stdlib:** write valid JSON when creating new database file ([46e0da2](https://github.com/SchoolyB/EZ/commit/46e0da26f15f7978bb05324a60d7adc3346237b3)), closes [#780](https://github.com/SchoolyB/EZ/issues/780)

## [0.30.0](https://github.com/SchoolyB/EZ/compare/v0.29.2...v0.30.0) (2025-12-21)


### Features

* **stdlib:** add [@db](https://github.com/db) module for simple key-value database ([342a4f9](https://github.com/SchoolyB/EZ/commit/342a4f922911cebf1a56eda176a83874b907cdf4))
* **stdlib:** add [@db](https://github.com/db) module for simple key-value database ([23e112a](https://github.com/SchoolyB/EZ/commit/23e112a3d9086ce9baf9ce66f6e8b936ed6c3932)), closes [#460](https://github.com/SchoolyB/EZ/issues/460)

## [0.29.2](https://github.com/SchoolyB/EZ/compare/v0.29.1...v0.29.2) (2025-12-21)


### Bug Fixes

* **cli:** consistent arg handling and remove stale `ez run` references ([8fcb687](https://github.com/SchoolyB/EZ/commit/8fcb687f7ef990aab376df653df3d14c29a0dc66))
* **cli:** consistent arg handling and remove stale `ez run` references ([0b7ba8c](https://github.com/SchoolyB/EZ/commit/0b7ba8c2dbba5968c557c7bc46b3f1113be72e59)), closes [#765](https://github.com/SchoolyB/EZ/issues/765)
* **language:** remove broken `private:module` and add typechecker validation ([3fcb311](https://github.com/SchoolyB/EZ/commit/3fcb31107049e1143186d3f468e7b9a75fa9f7b8))
* use existing E12001 instead of undefined E9020 ([09734b0](https://github.com/SchoolyB/EZ/commit/09734b0960a5383d5bfd37d2d4c9bb9663ea951f))
* use existing E12001 instead of undefined E9020 ([f959f49](https://github.com/SchoolyB/EZ/commit/f959f49b6f92fc65e21e7a87c87e02f9566f9af6)), closes [#769](https://github.com/SchoolyB/EZ/issues/769)
* **visibility:** remove broken private:module and add typechecker validation ([bca6f4c](https://github.com/SchoolyB/EZ/commit/bca6f4cdb5058bf60729fc72a3bf375cf27e9149)), closes [#767](https://github.com/SchoolyB/EZ/issues/767)

## [0.29.1](https://github.com/SchoolyB/EZ/compare/v0.29.0...v0.29.1) (2025-12-20)


### Bug Fixes

* **interpreter:** add bounds check for empty ReturnValue.Values ([69c1c39](https://github.com/SchoolyB/EZ/commit/69c1c39b14ad7ffc728fcb17e4f3979b8a7d043d))
* **interpreter:** add bounds check for empty ReturnValue.Values ([66859ca](https://github.com/SchoolyB/EZ/commit/66859cad7eca7b3f58bcc76e28064c32956b9d75)), closes [#740](https://github.com/SchoolyB/EZ/issues/740)
* **interpreter:** check Deref() error before compound assignment ([645af52](https://github.com/SchoolyB/EZ/commit/645af527f6e29700094504c890c38e2e0dd0d9a3))
* **interpreter:** check Deref() error before compound assignment ([836b7f7](https://github.com/SchoolyB/EZ/commit/836b7f71bcde48738ea16f7f67528bbc197bb958)), closes [#741](https://github.com/SchoolyB/EZ/issues/741)
* **parser:** prevent panic on comma-separated struct fields ([7886e20](https://github.com/SchoolyB/EZ/commit/7886e206e0b309821e4d3254b935d7aa123b9d66))
* **parser:** prevent panic on comma-separated struct fields ([aa68024](https://github.com/SchoolyB/EZ/commit/aa680242c9eb6b0317acd29ddb663054c38bac21)), closes [#750](https://github.com/SchoolyB/EZ/issues/750)
* **stdlib:** add bounds check for integer-to-byte conversion ([191ec8d](https://github.com/SchoolyB/EZ/commit/191ec8d7cc76739995ab150a937eee9f69e8d0e7))
* **stdlib:** add bounds check for integer-to-byte conversion ([26e214f](https://github.com/SchoolyB/EZ/commit/26e214fd72504dbeca12c470b4f3a7c6a1729470)), closes [#748](https://github.com/SchoolyB/EZ/issues/748)
* **stdlib:** make ignored file Close errors explicit in io.go ([c4048a9](https://github.com/SchoolyB/EZ/commit/c4048a9119e5e6fc51acd9a80b22bb5233cbbf0a))
* **stdlib:** make ignored file Close errors explicit in io.go ([52dd245](https://github.com/SchoolyB/EZ/commit/52dd245abae18f20a569d8dbae7296034218816e)), closes [#742](https://github.com/SchoolyB/EZ/issues/742)
* **stdlib:** remove redundant arrays.range() function ([f957fdd](https://github.com/SchoolyB/EZ/commit/f957fdd594212261739e1f9ce96dfb193f842c53))
* **stdlib:** remove redundant arrays.range() function ([6a2a7ec](https://github.com/SchoolyB/EZ/commit/6a2a7ec428f136deec22e6bd088f5109a0cc13e4)), closes [#746](https://github.com/SchoolyB/EZ/issues/746)
* **typechecker:** handle ignored error returns properly ([15d48a8](https://github.com/SchoolyB/EZ/commit/15d48a8528bd282fa4c896414d27c4b43dff3442))
* **typechecker:** handle ignored error returns properly ([5f18740](https://github.com/SchoolyB/EZ/commit/5f18740fd6a1c658e0bd4692106869db12712590)), closes [#752](https://github.com/SchoolyB/EZ/issues/752)

## [0.29.0](https://github.com/SchoolyB/EZ/compare/v0.28.3...v0.29.0) (2025-12-19)


### Features

* Struct field tags JSON customization ([ae64d0a](https://github.com/SchoolyB/EZ/commit/ae64d0aeb925d572b57c9a5898ed2753bcec0866))

## [0.28.3](https://github.com/SchoolyB/EZ/compare/v0.28.2...v0.28.3) (2025-12-19)


### Bug Fixes

* module symbol sharing and using statement resolution ([94eea8d](https://github.com/SchoolyB/EZ/commit/94eea8dac49e6c60a121d22a0d3f1316d7d231f0))
* module symbol sharing and using statement resolution ([2b7a0d0](https://github.com/SchoolyB/EZ/commit/2b7a0d021271e4a71f027b7aac3d86279f5eab91))

## [0.28.2](https://github.com/SchoolyB/EZ/compare/v0.28.1...v0.28.2) (2025-12-19)


### Bug Fixes

* show parser errors in imported modules instead of misleading undefined function errors ([e515f2c](https://github.com/SchoolyB/EZ/commit/e515f2c8bdc67bc84aef2a050500d83e3cb317d3))
* show parser errors in imported modules instead of misleading undefined function errors ([2592b1f](https://github.com/SchoolyB/EZ/commit/2592b1f6a51464f5aada3498a57c56db2c540172)), closes [#726](https://github.com/SchoolyB/EZ/issues/726)

## [0.28.1](https://github.com/SchoolyB/EZ/compare/v0.28.0...v0.28.1) (2025-12-19)


### Bug Fixes

* sort type checker errors by file and line number ([9ca37f6](https://github.com/SchoolyB/EZ/commit/9ca37f661b4d52121f42c27ddd6c14ac87b37f2a))
* sort type checker errors by file and line number ([c8e7f6b](https://github.com/SchoolyB/EZ/commit/c8e7f6bc67e2b119beadd6f37f2b90dffa4fa456)), closes [#727](https://github.com/SchoolyB/EZ/issues/727)

## [0.28.0](https://github.com/SchoolyB/EZ/compare/v0.27.0...v0.28.0) (2025-12-18)


### Features

* **lang:** add `cast()` keyword for type conversion ([0cc34f2](https://github.com/SchoolyB/EZ/commit/0cc34f24c469efaac6602765958c356eff36a4d7))
* **lang:** add cast() keyword for type conversion ([ab814f8](https://github.com/SchoolyB/EZ/commit/ab814f8ca127598625d37c0a1092ed9ef4a1054f)), closes [#717](https://github.com/SchoolyB/EZ/issues/717)
* **stdlib:** add [@binary](https://github.com/binary) module and sized type conversions ([496f874](https://github.com/SchoolyB/EZ/commit/496f87433c5f5f6a84f80af4b39f66194f309a6b))
* **stdlib:** add [@binary](https://github.com/binary) module and sized type conversions ([9487a65](https://github.com/SchoolyB/EZ/commit/9487a65fd48c8e9bb6a8ebcf9440fae5e3d14625)), closes [#716](https://github.com/SchoolyB/EZ/issues/716)


### Bug Fixes

* **modules:** add type checking for multi-file modules ([#722](https://github.com/SchoolyB/EZ/issues/722)) ([19b5006](https://github.com/SchoolyB/EZ/commit/19b50061bcc9054d653d94bc41e63e2d0cacaeda))
* **modules:** add type checking for multi-file modules ([#722](https://github.com/SchoolyB/EZ/issues/722)) ([d806280](https://github.com/SchoolyB/EZ/commit/d8062804910fe308d4a8886ac481b9bf45798009))
* **modules:** report type errors in single-file modules at check time ([#720](https://github.com/SchoolyB/EZ/issues/720)) ([72ec320](https://github.com/SchoolyB/EZ/commit/72ec320f48bc5ec1cb9b13fd0ab88a8f08de0e15))
* **modules:** report type errors in single-file modules at check time ([#720](https://github.com/SchoolyB/EZ/issues/720)) ([efcf797](https://github.com/SchoolyB/EZ/commit/efcf79757eb22c792cce539211c5a842751d756d))

## [0.27.0](https://github.com/SchoolyB/EZ/compare/v0.26.0...v0.27.0) (2025-12-18)


### Features

* **typechecker:** add type checking for all stdlib modules ([8842961](https://github.com/SchoolyB/EZ/commit/88429612f75394597e66db37d99180ea9e90d76d))
* **typechecker:** add type checking for all stdlib modules ([fc1f4e8](https://github.com/SchoolyB/EZ/commit/fc1f4e8364aeef6e43a2451629d010d542224dd6))


### Bug Fixes

* **typechecker:** comprehensive validation of imported types ([#709](https://github.com/SchoolyB/EZ/issues/709)) ([0aedff9](https://github.com/SchoolyB/EZ/commit/0aedff9e65b5d0919574f48bdb0dd5c650784f7e))
* **typechecker:** comprehensive validation of imported types ([#709](https://github.com/SchoolyB/EZ/issues/709)) ([88c32a7](https://github.com/SchoolyB/EZ/commit/88c32a7254e89a52e0a891eb7683266efb30a683))
* **typechecker:** for_each loop variables inherit mutability from collection ([fc7dd06](https://github.com/SchoolyB/EZ/commit/fc7dd0659c3cc63a864aa17c66a701157aa2520e))
* **typechecker:** resolve unqualified imported types in member access ([#706](https://github.com/SchoolyB/EZ/issues/706)) ([72f8bfc](https://github.com/SchoolyB/EZ/commit/72f8bfcde68df0de3bcf796cff8202d7c7b54c10))
* **typechecker:** resolve unqualified imported types in member access ([#706](https://github.com/SchoolyB/EZ/issues/706)) ([e6935f8](https://github.com/SchoolyB/EZ/commit/e6935f80b45949215101fa0300f2c367c940a87c))
* **typechecker:** validate field names in imported struct literals ([#708](https://github.com/SchoolyB/EZ/issues/708)) ([9ecc16b](https://github.com/SchoolyB/EZ/commit/9ecc16bb1d104ca2b00a3f3ed82c2860bb07b545))
* **typechecker:** validate field names in imported struct literals ([#708](https://github.com/SchoolyB/EZ/issues/708)) ([a14162b](https://github.com/SchoolyB/EZ/commit/a14162b9419700bace7d5c373fe47ad4faad01dd))

## [0.26.0](https://github.com/SchoolyB/EZ/compare/v0.25.0...v0.26.0) (2025-12-18)


### Features

* **parser:** support tuple unpacking in assignment statements ([#699](https://github.com/SchoolyB/EZ/issues/699)) ([#704](https://github.com/SchoolyB/EZ/issues/704)) ([1c01533](https://github.com/SchoolyB/EZ/commit/1c015336253968ce0d1655580103116de6aff52c))

## [0.25.0](https://github.com/SchoolyB/EZ/compare/v0.24.0...v0.25.0) (2025-12-18)


### Features

* multi-value handling improvements ([5b533d1](https://github.com/SchoolyB/EZ/commit/5b533d1a40ea3e3f3477f9a0805acd3a17113d39))


### Bug Fixes

* **interpreter:** display actual return type instead of RETURN_VALUE in E5012 errors ([e702d39](https://github.com/SchoolyB/EZ/commit/e702d396e2f17db6c6e9025fd5a473f4b7ba8729))
* **interpreter:** display actual return type instead of RETURN_VALUE in E5012 errors ([#696](https://github.com/SchoolyB/EZ/issues/696)) ([c84928e](https://github.com/SchoolyB/EZ/commit/c84928e2a3b632833738fdf98cf257322de2c8d5))
* **interpreter:** handle multi-value assignment errors correctly ([2f08c12](https://github.com/SchoolyB/EZ/commit/2f08c12ca9ca0c4852a249964fac49a917337b7e))
* **interpreter:** handle multi-value assignment errors correctly ([#698](https://github.com/SchoolyB/EZ/issues/698)) ([6270ad2](https://github.com/SchoolyB/EZ/commit/6270ad2a1d7786d0522f58c0a4371dee2a501aee))

## [0.24.0](https://github.com/SchoolyB/EZ/compare/v0.23.1...v0.24.0) (2025-12-17)


### Features

* add W2010 warning for chained member access on nullable structs ([#689](https://github.com/SchoolyB/EZ/issues/689)) ([cd57753](https://github.com/SchoolyB/EZ/commit/cd57753bd3858e2e8b33ca230661c9c23b416934))
* add W2010 warning for chained member access on nullable structs ([#689](https://github.com/SchoolyB/EZ/issues/689)) ([3cd1ede](https://github.com/SchoolyB/EZ/commit/3cd1ede848574aa97f0b697905ffce283a7d713b))
* implement ref() builtin and copy-by-default semantics ([#661](https://github.com/SchoolyB/EZ/issues/661)) ([743153c](https://github.com/SchoolyB/EZ/commit/743153cee33eb181622433e489dc0fa94d62a701))
* implement ref() builtin and copy-by-default semantics ([#661](https://github.com/SchoolyB/EZ/issues/661)) ([d064e56](https://github.com/SchoolyB/EZ/commit/d064e56e894206ba2a2074a03f75bca15949de14))
* **typechecker:** comprehensive typechecker overhaul with ref() builtin ([e05a459](https://github.com/SchoolyB/EZ/commit/e05a4591c8be5a5a0f99eb04fe833fd3542e7021))
* **typechecker:** detect literal division/modulo by zero ([8ce1a11](https://github.com/SchoolyB/EZ/commit/8ce1a1124f8de946cd6f283b427eb242a0e97faf))
* **typechecker:** detect literal division/modulo by zero ([#667](https://github.com/SchoolyB/EZ/issues/667)) ([76b4f1e](https://github.com/SchoolyB/EZ/commit/76b4f1e2da6d955787e394fb1fab07eb872b8e0a))
* **typechecker:** detect undefined variables and functions at check time ([#663](https://github.com/SchoolyB/EZ/issues/663)) ([4ca2c68](https://github.com/SchoolyB/EZ/commit/4ca2c68a56b82fc2917f4121373ff862bf715fdd))
* **typechecker:** detect undefined variables and functions at check time ([#663](https://github.com/SchoolyB/EZ/issues/663)) ([5334c4b](https://github.com/SchoolyB/EZ/commit/5334c4bb39363c1ec27994991d01ebc4792f6591))
* **typechecker:** reject executable statements at file scope ([c2b372f](https://github.com/SchoolyB/EZ/commit/c2b372f0ec6ecbd0868a8a75b81d8fa2561abe1e))
* **typechecker:** reject executable statements at file scope ([#662](https://github.com/SchoolyB/EZ/issues/662)) ([9ec3cd0](https://github.com/SchoolyB/EZ/commit/9ec3cd0c4155840dc1fa21f17a838c10fe470ce7))
* **typechecker:** validate integer literal ranges for sized types ([c315995](https://github.com/SchoolyB/EZ/commit/c3159952bd246079c6671e0883b2c4ae8867b03b))
* **typechecker:** validate integer literal ranges for sized types ([#666](https://github.com/SchoolyB/EZ/issues/666)) ([0d7cdfe](https://github.com/SchoolyB/EZ/commit/0d7cdfea655141e0a31359f17e66f95418072b91))


### Bug Fixes

* add type inference for stdlib module multi-return functions ([c2be2c1](https://github.com/SchoolyB/EZ/commit/c2be2c14d2cc8040e4368a7e94a912c16464782d))
* add type inference for stdlib module multi-return functions ([f5120f8](https://github.com/SchoolyB/EZ/commit/f5120f8c5594e64fb0856dd4bd01bb3d1c4ed1cb))
* detect missing return on all code paths at check time ([860be2a](https://github.com/SchoolyB/EZ/commit/860be2a8843fd5f6a1a7821f64241b41e43f4b64))
* detect missing return on all code paths at check time ([81667b9](https://github.com/SchoolyB/EZ/commit/81667b9707f2cad25c5802da7be9a74cd15d26d1)), closes [#660](https://github.com/SchoolyB/EZ/issues/660)
* properly type multi-return builtin functions like read_int() ([70519bc](https://github.com/SchoolyB/EZ/commit/70519bc5717aedd6cfc1135bc25790c0feb354b1))
* properly type multi-return builtin functions like read_int() ([a88577e](https://github.com/SchoolyB/EZ/commit/a88577e2cac2e8233df18b25345b53fdc3f9a4b2))
* support module constants via using directive ([#677](https://github.com/SchoolyB/EZ/issues/677)) ([a493e46](https://github.com/SchoolyB/EZ/commit/a493e461198baad719b48c9fe3109dfad183c23d))
* support module constants via using directive ([#677](https://github.com/SchoolyB/EZ/issues/677)) ([70dbfc3](https://github.com/SchoolyB/EZ/commit/70dbfc362b9948cd10efc08fdcc567b59aa20819))
* **typechecker:** add check-time array bounds checking ([#685](https://github.com/SchoolyB/EZ/issues/685)) ([9fb99de](https://github.com/SchoolyB/EZ/commit/9fb99ded85c0e18e6539deccd5cea722e603e3fb))
* **typechecker:** add check-time array bounds checking ([#685](https://github.com/SchoolyB/EZ/issues/685)) ([c150246](https://github.com/SchoolyB/EZ/commit/c1502462ea431098d9c6afee0e52dfc5b8a51f26))
* **typechecker:** add warning for member access on error type ([#687](https://github.com/SchoolyB/EZ/issues/687)) ([052ead9](https://github.com/SchoolyB/EZ/commit/052ead9c9159f73d485600ed4cb6e4368800e126))
* **typechecker:** add warning for member access on error type ([#687](https://github.com/SchoolyB/EZ/issues/687)) ([189a14c](https://github.com/SchoolyB/EZ/commit/189a14c8fb669fb89bb4952ce83eb02e3b153779))
* **typechecker:** detect undefined variables in assignment targets ([f467bcf](https://github.com/SchoolyB/EZ/commit/f467bcfcf834b3f0c89506decd42d3532b7aa9df))
* **typechecker:** detect undefined variables in assignment targets ([#665](https://github.com/SchoolyB/EZ/issues/665)) ([24cf9b1](https://github.com/SchoolyB/EZ/commit/24cf9b11b46ede1acf6e8e3f090300da9e377546))
* **typechecker:** extend overflow detection to all integer types ([#686](https://github.com/SchoolyB/EZ/issues/686)) ([c56aa3d](https://github.com/SchoolyB/EZ/commit/c56aa3d22302f93c5a3f8e60a17f382a94e20f36))
* **typechecker:** extend overflow detection to all integer types ([#686](https://github.com/SchoolyB/EZ/issues/686)) ([6e0b31a](https://github.com/SchoolyB/EZ/commit/6e0b31a1f5d1bbf3a332e53324391a9da3e4f84c))
* **typechecker:** infer types for module variables via using directive ([#677](https://github.com/SchoolyB/EZ/issues/677)) ([584d42e](https://github.com/SchoolyB/EZ/commit/584d42eedafcd97fefb2c731ee7108d2d3c3ea4b))
* **typechecker:** resolve user module functions via 'using' directive ([b90830e](https://github.com/SchoolyB/EZ/commit/b90830e4bea45b86cabe3aef4d0d021bad617729))
* **typechecker:** resolve user module functions via 'using' directive ([#671](https://github.com/SchoolyB/EZ/issues/671)) ([1285737](https://github.com/SchoolyB/EZ/commit/1285737733f4f2c9ae5bcfec0cee70fe0ec9a864))
* **typechecker:** validate expressions in string interpolations ([#684](https://github.com/SchoolyB/EZ/issues/684)) ([a4d8990](https://github.com/SchoolyB/EZ/commit/a4d8990b53e5a689bc06f40815265f0230518a5d))
* **typechecker:** validate expressions in string interpolations ([#684](https://github.com/SchoolyB/EZ/issues/684)) ([4da234d](https://github.com/SchoolyB/EZ/commit/4da234de0f6214635e766ae6da8dfd4a3e351d05))

## [0.23.1](https://github.com/SchoolyB/EZ/compare/v0.23.0...v0.23.1) (2025-12-17)


### Bug Fixes

* allow nil return for error type in user-defined functions ([4d78d05](https://github.com/SchoolyB/EZ/commit/4d78d050ba9d314303f239c6f8f96e520bd55a51))
* allow nil return for error type in user-defined functions ([f0fd24a](https://github.com/SchoolyB/EZ/commit/f0fd24a8bd821d782427ba30dfd42fc69ec129b3)), closes [#657](https://github.com/SchoolyB/EZ/issues/657)

## [0.23.0](https://github.com/SchoolyB/EZ/compare/v0.22.6...v0.23.0) (2025-12-17)


### Features

* **stdlib:** add `strings.to_int()`, `strings.to_float()`, `strings.to_bool()` ([846f90a](https://github.com/SchoolyB/EZ/commit/846f90af5f781c96bc13e983d4e2e183e30d6dd4))
* **stdlib:** add strings.to_int(), strings.to_float(), strings.to_bool() ([e496f23](https://github.com/SchoolyB/EZ/commit/e496f231bafb51979f7127a7c8a26516df365afb)), closes [#651](https://github.com/SchoolyB/EZ/issues/651)

## [0.22.6](https://github.com/SchoolyB/EZ/compare/v0.22.5...v0.22.6) (2025-12-16)


### Bug Fixes

* **stdlib:** `arrays.set()` now modifies array in place ([411c17f](https://github.com/SchoolyB/EZ/commit/411c17f085cb3ffe342a62d46bd318e5c898680c))
* **stdlib:** arrays.set() now modifies array in-place ([2cdb73a](https://github.com/SchoolyB/EZ/commit/2cdb73a58be0a24dd92f41b26f9ba655cdbbb8fd)), closes [#652](https://github.com/SchoolyB/EZ/issues/652)

## [0.22.5](https://github.com/SchoolyB/EZ/compare/v0.22.4...v0.22.5) (2025-12-16)


### Bug Fixes

* cross-module nested struct initialization ([a22d7e3](https://github.com/SchoolyB/EZ/commit/a22d7e36822d957f741a578ee1f5df694480e503))
* cross-module nested struct initialization ([13cf3e0](https://github.com/SchoolyB/EZ/commit/13cf3e0d46325920a59696df767a736cc473f5c5))

## [0.22.4](https://github.com/SchoolyB/EZ/compare/v0.22.3...v0.22.4) (2025-12-16)


### Bug Fixes

* workflow rebase, add README badges, improve test coverage ([d356bce](https://github.com/SchoolyB/EZ/commit/d356bcef43c84c48ddabcf09e501dd50c82fffa8))

## [0.22.3](https://github.com/SchoolyB/EZ/compare/v0.22.2...v0.22.3) (2025-12-16)


### Bug Fixes

* version update detection and error sync workflow ([fbdb7bd](https://github.com/SchoolyB/EZ/commit/fbdb7bd421d6419452fa901940d5c6a950cacf2e))
* version update detection and error sync workflow ([f773ddb](https://github.com/SchoolyB/EZ/commit/f773ddb0af517295dadf3dc3f747ebe26970b53d))

## [0.22.2](https://github.com/SchoolyB/EZ/compare/v0.22.1...v0.22.2) (2025-12-16)


### Bug Fixes

* [@strict](https://github.com/strict) when enforces enum exhaustiveness at check time ([#629](https://github.com/SchoolyB/EZ/issues/629)) ([f549a3b](https://github.com/SchoolyB/EZ/commit/f549a3bd63c013f13cdb3bb4987f061ff794a0d1))
* [@strict](https://github.com/strict) when rejects non-enum expressions ([#628](https://github.com/SchoolyB/EZ/issues/628)) ([c734b18](https://github.com/SchoolyB/EZ/commit/c734b1845b109643f8aa1c5d7acb91fab7e3c232))
* [@strict](https://github.com/strict) when rejects non-enum expressions in cases ([#628](https://github.com/SchoolyB/EZ/issues/628)) ([799b7a7](https://github.com/SchoolyB/EZ/commit/799b7a7fd3035eae677fb9388d25eef06d09fa1a))
* `[@strict](https://github.com/strict)` when enforces enum exhaustiveness at check time ([#629](https://github.com/SchoolyB/EZ/issues/629)) ([be87d59](https://github.com/SchoolyB/EZ/commit/be87d591d8c4357f87f6700196b107976df19e91))
* duplicate map keys in literal now produce check-time error ([#641](https://github.com/SchoolyB/EZ/issues/641)) ([06b3f91](https://github.com/SchoolyB/EZ/commit/06b3f91df8e8add8e7a020a50d9bd60cea691482))
* duplicate map keys in literal now produce check-time error ([#641](https://github.com/SchoolyB/EZ/issues/641)) ([f011903](https://github.com/SchoolyB/EZ/commit/f0119037c23adb2d7ebd610b347bf10453d7bb88))
* float display now shows actual precision for debugging ([#640](https://github.com/SchoolyB/EZ/issues/640)) ([d2051fb](https://github.com/SchoolyB/EZ/commit/d2051fbce7ab28af8e3016c527766ec0b75bc186))
* float display now shows actual precision for debugging ([#640](https://github.com/SchoolyB/EZ/issues/640)) ([3ef9314](https://github.com/SchoolyB/EZ/commit/3ef93147f3104321000e65e39ebdaf7f55b7318d))
* recursively initialize nested struct fields ([#621](https://github.com/SchoolyB/EZ/issues/621)) ([ad4f911](https://github.com/SchoolyB/EZ/commit/ad4f911fbd6308544fcf67970280839baad41089))
* recursively initialize nested struct fields ([#621](https://github.com/SchoolyB/EZ/issues/621)) ([3b7c653](https://github.com/SchoolyB/EZ/commit/3b7c65385280bd48f58b505b42f6c0850e863cce))
* validate type assignments for imported module struct fields ([#620](https://github.com/SchoolyB/EZ/issues/620)) ([194d74f](https://github.com/SchoolyB/EZ/commit/194d74fa917c8690bb0baf68392447d1b6cf8089))
* validate type assignments for imported module struct fields ([#620](https://github.com/SchoolyB/EZ/issues/620)) ([a965fb3](https://github.com/SchoolyB/EZ/commit/a965fb3a239bf82385c1752494ba844fa33b5b80))

## [0.22.1](https://github.com/SchoolyB/EZ/compare/v0.22.0...v0.22.1) (2025-12-15)


### Bug Fixes

* detect variable shadowing of functions from used modules ([db505b4](https://github.com/SchoolyB/EZ/commit/db505b40bd022a64e31752f08f1b59ad02e9bfe2))
* detect variable shadowing of functions from used modules ([#616](https://github.com/SchoolyB/EZ/issues/616)) ([cf40e75](https://github.com/SchoolyB/EZ/commit/cf40e75abffaee9d9a9553bc652014bda149f07e))

## [0.22.0](https://github.com/SchoolyB/EZ/compare/v0.21.2...v0.22.0) (2025-12-15)


### Features

* add `@JSON` module, raw strings, and restrict `any` type ([8e566e5](https://github.com/SchoolyB/EZ/commit/8e566e5c73e9cd14c595f7b63dbed93104745f1f))
* add JSON module, raw strings, and restrict 'any' type ([f66b734](https://github.com/SchoolyB/EZ/commit/f66b734823d38dc9c40312044e25905cda096374))

## [0.21.2](https://github.com/SchoolyB/EZ/compare/v0.21.1...v0.21.2) (2025-12-15)


### Bug Fixes

* December 15, 2025 bug fixes ([#580](https://github.com/SchoolyB/EZ/issues/580)) ([dd6253c](https://github.com/SchoolyB/EZ/commit/dd6253c1a8ccdeed95386b5c2a2418d7b8be0aad))

## [0.21.1](https://github.com/SchoolyB/EZ/compare/v0.21.0...v0.21.1) (2025-12-14)


### Bug Fixes

* December 14, 2025 bug fixes ([#544](https://github.com/SchoolyB/EZ/issues/544)) ([3169059](https://github.com/SchoolyB/EZ/commit/31690596cf470115b4c4269d1ac6d24519c15296))

## [0.21.0](https://github.com/SchoolyB/EZ/compare/v0.20.1...v0.21.0) (2025-12-12)


### Features

* global builtins, [@std](https://github.com/std) expansion, and bug fixes ([#525](https://github.com/SchoolyB/EZ/issues/525), [#526](https://github.com/SchoolyB/EZ/issues/526), [#522](https://github.com/SchoolyB/EZ/issues/522), [#523](https://github.com/SchoolyB/EZ/issues/523), [#524](https://github.com/SchoolyB/EZ/issues/524), [#527](https://github.com/SchoolyB/EZ/issues/527)) ([#532](https://github.com/SchoolyB/EZ/issues/532)) ([accd080](https://github.com/SchoolyB/EZ/commit/accd0803e711b1327d2f4b0ee6c334f04c600846))

## [0.20.1](https://github.com/SchoolyB/EZ/compare/v0.20.0...v0.20.1) (2025-12-12)


### Bug Fixes

* december 12 patch release ([#520](https://github.com/SchoolyB/EZ/issues/520)) ([9e75aa0](https://github.com/SchoolyB/EZ/commit/9e75aa07bb6687d01ce471efa5bbaafd11f9c5c3))

## [0.20.0](https://github.com/SchoolyB/EZ/compare/v0.19.3...v0.20.0) (2025-12-11)


### Features

* allow range() in if/in expressions and when/is statements ([#501](https://github.com/SchoolyB/EZ/issues/501)) ([#505](https://github.com/SchoolyB/EZ/issues/505)) ([de2890f](https://github.com/SchoolyB/EZ/commit/de2890f16bcd738adca6de3803d93c8e1dabddef))

## [0.19.3](https://github.com/SchoolyB/EZ/compare/v0.19.2...v0.19.3) (2025-12-11)


### Bug Fixes

* remove [@string](https://github.com/string) alias and add module suggestion hints ([#502](https://github.com/SchoolyB/EZ/issues/502)) ([#503](https://github.com/SchoolyB/EZ/issues/503)) ([53122a1](https://github.com/SchoolyB/EZ/commit/53122a1350104efae0bed292167851a34e04d4a6))

## [0.19.2](https://github.com/SchoolyB/EZ/compare/v0.19.1...v0.19.2) (2025-12-11)


### Bug Fixes

* show update notification immediately on all commands ([#499](https://github.com/SchoolyB/EZ/issues/499)) ([c436b2f](https://github.com/SchoolyB/EZ/commit/c436b2fe91d723317f54c5021499f45f94934ac7)), closes [#498](https://github.com/SchoolyB/EZ/issues/498)

## [0.19.1](https://github.com/SchoolyB/EZ/compare/v0.19.0...v0.19.1) (2025-12-11)


### Bug Fixes

* add path validation to archive extraction functions ([#487](https://github.com/SchoolyB/EZ/issues/487)) ([#495](https://github.com/SchoolyB/EZ/issues/495)) ([974250a](https://github.com/SchoolyB/EZ/commit/974250a0f45c8cbee29039c8b5e8ed002283f736))

## [0.19.0](https://github.com/SchoolyB/EZ/compare/v0.18.1...v0.19.0) (2025-12-11)


### Features

* add when/is switch statements ([#179](https://github.com/SchoolyB/EZ/issues/179)) ([#491](https://github.com/SchoolyB/EZ/issues/491)) ([4f0c068](https://github.com/SchoolyB/EZ/commit/4f0c0689c8efcf3b2dbf8bd08764fb5b0fa510eb))

## [0.18.1](https://github.com/SchoolyB/EZ/compare/v0.18.0...v0.18.1) (2025-12-11)


### Bug Fixes

* correct error codes for immutable variable/map errors ([#488](https://github.com/SchoolyB/EZ/issues/488)) ([727ce1b](https://github.com/SchoolyB/EZ/commit/727ce1bce576f0628aef67c1e7dd500a4c24e7d1))

## [0.18.0](https://github.com/SchoolyB/EZ/compare/v0.17.2...v0.18.0) (2025-12-10)


### Features

* add default parameter values for functions ([#312](https://github.com/SchoolyB/EZ/issues/312)) ([#485](https://github.com/SchoolyB/EZ/issues/485)) ([933ca6f](https://github.com/SchoolyB/EZ/commit/933ca6fe278654cfea9a1172e4a3eb0419f05f58))

## [0.17.2](https://github.com/SchoolyB/EZ/compare/v0.17.1...v0.17.2) (2025-12-10)


### Bug Fixes

* auto-elevate to sudo when update needs root permissions ([#483](https://github.com/SchoolyB/EZ/issues/483)) ([8cfa5c3](https://github.com/SchoolyB/EZ/commit/8cfa5c3d2814d8ec2fa7c2593ab405829e80bdb9))

## [0.17.1](https://github.com/SchoolyB/EZ/compare/v0.17.0...v0.17.1) (2025-12-10)


### Bug Fixes

* handle .tar.gz/.zip archives in ez update ([#481](https://github.com/SchoolyB/EZ/issues/481)) ([b7d4314](https://github.com/SchoolyB/EZ/commit/b7d43143472a1436037fa79e63efb396e4e3126f))

## [0.17.0](https://github.com/SchoolyB/EZ/compare/v0.16.15...v0.17.0) (2025-12-10)


### Features

* add update checker and `ez update` command ([#478](https://github.com/SchoolyB/EZ/issues/478)) ([#479](https://github.com/SchoolyB/EZ/issues/479)) ([a33c92b](https://github.com/SchoolyB/EZ/commit/a33c92be20dc111bf0d8a1529b7a06b7f3b7522b))

## [0.16.15](https://github.com/SchoolyB/EZ/compare/v0.16.14...v0.16.15) (2025-12-10)


### Bug Fixes

* show correct file location for multi-file module errors ([#466](https://github.com/SchoolyB/EZ/issues/466)) ([#476](https://github.com/SchoolyB/EZ/issues/476)) ([b187e1a](https://github.com/SchoolyB/EZ/commit/b187e1a6b8e98347acc541775eb27d6d59c98869))

## [0.16.14](https://github.com/SchoolyB/EZ/compare/v0.16.13...v0.16.14) (2025-12-10)


### Bug Fixes

* show file location in module not found error ([#461](https://github.com/SchoolyB/EZ/issues/461)) ([#474](https://github.com/SchoolyB/EZ/issues/474)) ([a6eec23](https://github.com/SchoolyB/EZ/commit/a6eec2353111ce07adfca2733e93d58afe352c3d))

## [0.16.13](https://github.com/SchoolyB/EZ/compare/v0.16.12...v0.16.13) (2025-12-10)


### Bug Fixes

* suppress module name warning for files in matching directories ([#464](https://github.com/SchoolyB/EZ/issues/464)) ([#472](https://github.com/SchoolyB/EZ/issues/472)) ([6be1062](https://github.com/SchoolyB/EZ/commit/6be106280f0cd375a9a93dac8197b6ab4fe34c2e))

## [0.16.12](https://github.com/SchoolyB/EZ/compare/v0.16.11...v0.16.12) (2025-12-10)


### Bug Fixes

* handle module-prefixed types in type compatibility checks ([#463](https://github.com/SchoolyB/EZ/issues/463)) ([#469](https://github.com/SchoolyB/EZ/issues/469)) ([3c597de](https://github.com/SchoolyB/EZ/commit/3c597dec48fafc0a2cdb9c2fadee796f04bb73ac))

## [0.16.11](https://github.com/SchoolyB/EZ/compare/v0.16.10...v0.16.11) (2025-12-10)


### Bug Fixes

* resolve uppercase constants being parsed as struct literals ([#462](https://github.com/SchoolyB/EZ/issues/462)) ([a406de3](https://github.com/SchoolyB/EZ/commit/a406de3d496cf89c4f405182d5392b16405c6fc4))

## [0.16.10](https://github.com/SchoolyB/EZ/compare/v0.16.9...v0.16.10) (2025-12-09)


### Bug Fixes

* bug fixes batch - parser, stdlib, interpreter, and enum map keys ([#454](https://github.com/SchoolyB/EZ/issues/454)) ([f90e10f](https://github.com/SchoolyB/EZ/commit/f90e10fd02b3946ac37341956b453db744198017)), closes [#452](https://github.com/SchoolyB/EZ/issues/452)

## [0.16.9](https://github.com/SchoolyB/EZ/compare/v0.16.8...v0.16.9) (2025-12-08)


### Bug Fixes

* implement arbitrary precision integers for i128/u128 support ([#437](https://github.com/SchoolyB/EZ/issues/437)) ([#440](https://github.com/SchoolyB/EZ/issues/440)) ([af4cdbf](https://github.com/SchoolyB/EZ/commit/af4cdbfd42edcd87d5982032d06cc913cc01e75f))

## [0.16.8](https://github.com/SchoolyB/EZ/compare/v0.16.7...v0.16.8) (2025-12-08)


### Bug Fixes

* integration test overhaul and bug fixes ([#435](https://github.com/SchoolyB/EZ/issues/435)) ([a4ad4e8](https://github.com/SchoolyB/EZ/commit/a4ad4e8549490a5cf03b8d54bd9b48511a3af264))

## [0.16.7](https://github.com/SchoolyB/EZ/compare/v0.16.6...v0.16.7) (2025-12-08)


### Bug Fixes

* detect integer overflow in negation and division ([#424](https://github.com/SchoolyB/EZ/issues/424)) ([e83bdfe](https://github.com/SchoolyB/EZ/commit/e83bdfef81ab73cad1d2b5d9062b1a8be071f2d8))

## [0.16.6](https://github.com/SchoolyB/EZ/compare/v0.16.5...v0.16.6) (2025-12-08)


### Bug Fixes

* stdlib functions preserve input type ([#422](https://github.com/SchoolyB/EZ/issues/422)) ([1e91801](https://github.com/SchoolyB/EZ/commit/1e91801ff35219dbdee45e87ae6a4af4be9453eb)), closes [#404](https://github.com/SchoolyB/EZ/issues/404)

## [0.16.5](https://github.com/SchoolyB/EZ/compare/v0.16.4...v0.16.5) (2025-12-08)


### Bug Fixes

* float division by zero returns INF per IEEE 754 ([#420](https://github.com/SchoolyB/EZ/issues/420)) ([744cf75](https://github.com/SchoolyB/EZ/commit/744cf75b2f9188103cfd4e4734900b364c3a4781)), closes [#402](https://github.com/SchoolyB/EZ/issues/402)

## [0.16.4](https://github.com/SchoolyB/EZ/compare/v0.16.3...v0.16.4) (2025-12-08)


### Bug Fixes

* allow byte to int conversion with int() ([#418](https://github.com/SchoolyB/EZ/issues/418)) ([33dd463](https://github.com/SchoolyB/EZ/commit/33dd463d19ed16fe36f03fa3b9aba641c56edffb)), closes [#403](https://github.com/SchoolyB/EZ/issues/403)

## [0.16.3](https://github.com/SchoolyB/EZ/compare/v0.16.2...v0.16.3) (2025-12-08)


### Bug Fixes

* reject nil assignment to non-nullable types ([#416](https://github.com/SchoolyB/EZ/issues/416)) ([40e82e3](https://github.com/SchoolyB/EZ/commit/40e82e3f7addc2410ffa0a3ec062c4f5184a34f0)), closes [#407](https://github.com/SchoolyB/EZ/issues/407)

## [0.16.2](https://github.com/SchoolyB/EZ/compare/v0.16.1...v0.16.2) (2025-12-08)


### Bug Fixes

* detect mixed-type enums at check time ([#414](https://github.com/SchoolyB/EZ/issues/414)) ([e1b8c63](https://github.com/SchoolyB/EZ/commit/e1b8c63fd7c841d8d3aea2ad48b0d2d31483e6ca)), closes [#410](https://github.com/SchoolyB/EZ/issues/410)

## [0.16.1](https://github.com/SchoolyB/EZ/compare/v0.16.0...v0.16.1) (2025-12-08)


### Bug Fixes

* make array functions modify in-place and fix remove() API ([#412](https://github.com/SchoolyB/EZ/issues/412)) ([f6890b8](https://github.com/SchoolyB/EZ/commit/f6890b82553549702b3d52186843ca7c11e2860d))

## [0.16.0](https://github.com/SchoolyB/EZ/compare/v0.15.2...v0.16.0) (2025-12-07)


### Features

* add line editor for REPL with arrow key navigation and history ([#400](https://github.com/SchoolyB/EZ/issues/400)) ([bce7343](https://github.com/SchoolyB/EZ/commit/bce7343118564ec2f8b7b2e79b2eec3cd0b49711))

## [0.15.2](https://github.com/SchoolyB/EZ/compare/v0.15.1...v0.15.2) (2025-12-07)


### Bug Fixes

* resolve stdlib bugs for arrays, strings, and math modules ([#398](https://github.com/SchoolyB/EZ/issues/398)) ([b278ce6](https://github.com/SchoolyB/EZ/commit/b278ce6744cba9c3e8bf22237038f8cce398bda8))

## [0.15.1](https://github.com/SchoolyB/EZ/compare/v0.15.0...v0.15.1) (2025-12-07)


### Bug Fixes

* resolve several interpreter bugs ([5c083d3](https://github.com/SchoolyB/EZ/commit/5c083d33e3d0f18cef30049f3f57e184ce131d78))

## [0.15.0](https://github.com/SchoolyB/EZ/compare/v0.14.10...v0.15.0) (2025-12-07)


### Features

* replace [@ignore](https://github.com/ignore) with _ (underscore) blank identifier ([#376](https://github.com/SchoolyB/EZ/issues/376)) ([66111be](https://github.com/SchoolyB/EZ/commit/66111beaf80ca72dab092a9b0e62b1fa5e4da58a))

## [0.14.10](https://github.com/SchoolyB/EZ/compare/v0.14.9...v0.14.10) (2025-12-07)


### Bug Fixes

* resolve multiple bugs in stdlib, lexer, and parser ([#374](https://github.com/SchoolyB/EZ/issues/374)) ([c4be966](https://github.com/SchoolyB/EZ/commit/c4be9660ed9ced0f6a812d5a98ef5eea9389a813))

## [0.14.9](https://github.com/SchoolyB/EZ/compare/v0.14.8...v0.14.9) (2025-12-05)


### Bug Fixes

* **interpreter:** nested mutable parameter forwarding now works correctly ([#367](https://github.com/SchoolyB/EZ/issues/367)) ([5762939](https://github.com/SchoolyB/EZ/commit/57629390fb7bd4a9c53b55d9a259f853841de901)), closes [#338](https://github.com/SchoolyB/EZ/issues/338)

## [0.14.8](https://github.com/SchoolyB/EZ/compare/v0.14.7...v0.14.8) (2025-12-05)


### Bug Fixes

* **typechecker:** type errors now report correct source location ([#362](https://github.com/SchoolyB/EZ/issues/362)) ([13cdb4e](https://github.com/SchoolyB/EZ/commit/13cdb4ecd40f282c01749bf0f0ff65a22b6ea011))

## [0.14.7](https://github.com/SchoolyB/EZ/compare/v0.14.6...v0.14.7) (2025-12-05)


### Bug Fixes

* **parser:** handle minimum int64 literal (-9223372036854775808) ([#360](https://github.com/SchoolyB/EZ/issues/360)) ([8c75b43](https://github.com/SchoolyB/EZ/commit/8c75b434ff40f3e11066edbeb13a563e03a43b76))

## [0.14.6](https://github.com/SchoolyB/EZ/compare/v0.14.5...v0.14.6) (2025-12-05)


### Bug Fixes

* **parser:** enum member access in if condition no longer causes parser error ([#358](https://github.com/SchoolyB/EZ/issues/358)) ([6e0c5de](https://github.com/SchoolyB/EZ/commit/6e0c5de28bc3ba4e287bd1bbbb92ac5abd126fc8))

## [0.14.5](https://github.com/SchoolyB/EZ/compare/v0.14.4...v0.14.5) (2025-12-05)


### Bug Fixes

* **evaluator:** isTruthy now checks Boolean.Value instead of pointer identity ([#354](https://github.com/SchoolyB/EZ/issues/354)) ([18edd78](https://github.com/SchoolyB/EZ/commit/18edd78036eb4c57637303283729496f2d3c03b1))

## [0.14.4](https://github.com/SchoolyB/EZ/compare/v0.14.3...v0.14.4) (2025-12-05)


### Bug Fixes

* **ci:** auto-merge release PRs even when a release is created in same run ([eabee09](https://github.com/SchoolyB/EZ/commit/eabee09ea4800cc6618924636b5ed1511b2f25e8))
* **stdlib:** arrays.insert() and arrays.remove() now modify array in-place ([3ad569a](https://github.com/SchoolyB/EZ/commit/3ad569a9a0e3b3b39664335551d7d0e2cfbf89e2))
* **stdlib:** arrays.insert() and arrays.remove() now modify array in-place ([f26797d](https://github.com/SchoolyB/EZ/commit/f26797ddcd2a2be3ba23f06384b3b1e3ceb4330a))

## [0.14.3](https://github.com/SchoolyB/EZ/compare/v0.14.2...v0.14.3) (2025-12-05)


### Bug Fixes

* **evaluator:** implement short-circuit evaluation for && and || ([a9e4fe1](https://github.com/SchoolyB/EZ/commit/a9e4fe13877775af1a2f7859cc218484a31909b2))
* **evaluator:** implement short-circuit evaluation for && and || ([2f6f0a6](https://github.com/SchoolyB/EZ/commit/2f6f0a6bdc10484e58ade9b54c2a45ca4acd3a25))

## [0.14.2](https://github.com/SchoolyB/EZ/compare/v0.14.1...v0.14.2) (2025-12-05)


### Bug Fixes

* **typechecker:** handle array and map types in struct fields ([0455540](https://github.com/SchoolyB/EZ/commit/04555409b90e3bcc90825f2915348eecc84e6b40))
* **typechecker:** handle array and map types in struct fields ([0d1cd53](https://github.com/SchoolyB/EZ/commit/0d1cd53cd6d738c969c4beccfad56ba49f18ddd1))

## [0.14.1](https://github.com/SchoolyB/EZ/compare/v0.14.0...v0.14.1) (2025-12-04)


### Bug Fixes

* **interpreter:** add recursion depth limit to prevent stack overflow ([ccda7b7](https://github.com/SchoolyB/EZ/commit/ccda7b779bc8534b00f3e6a5f8396b4a7c574231)), closes [#327](https://github.com/SchoolyB/EZ/issues/327)
* **lexer:** preserve line numbers in string interpolation expressions ([5a236b7](https://github.com/SchoolyB/EZ/commit/5a236b72949fb37a54a4acdcb65cbe8069978f07)), closes [#323](https://github.com/SchoolyB/EZ/issues/323)
* **parser:** block reserved names as function parameter names ([1a52eb0](https://github.com/SchoolyB/EZ/commit/1a52eb00148ccf97b2e80684183d541335a12985))
* **parser:** disallow import statements inside blocks and after declarations ([19118f6](https://github.com/SchoolyB/EZ/commit/19118f6eddcecd4632c9f1d893fe78ab90251d51)), closes [#324](https://github.com/SchoolyB/EZ/issues/324)
* **parser:** prevent nil pointer crash when using 'const' as identifier ([e2177b3](https://github.com/SchoolyB/EZ/commit/e2177b389aed3acd022e8214387146609d1b6e17)), closes [#317](https://github.com/SchoolyB/EZ/issues/317)
* **parser:** use helpful error when keywords used as identifiers ([614d2bd](https://github.com/SchoolyB/EZ/commit/614d2bda79524de9348734bbaa42c9be2ca86f0b))
* **parser:** use helpful error when keywords used as identifiers ([5ffb6e3](https://github.com/SchoolyB/EZ/commit/5ffb6e393445ae14bf806bbaa1f3baa39174746a)), closes [#326](https://github.com/SchoolyB/EZ/issues/326)
* **parser:** use specific error codes for struct/enum reserved names ([c86b903](https://github.com/SchoolyB/EZ/commit/c86b9038ca1e85e46e77b93d90a8a1d56236ec4a))
* **parser:** validate enum value names against reserved keywords ([1a3f9b1](https://github.com/SchoolyB/EZ/commit/1a3f9b18df2107bd2806fdd9b525461ffd3f2c10)), closes [#322](https://github.com/SchoolyB/EZ/issues/322)
* **parser:** validate struct field names against reserved keywords ([a077535](https://github.com/SchoolyB/EZ/commit/a077535e905202e19dc34fd696f02e4bc51f59d9)), closes [#321](https://github.com/SchoolyB/EZ/issues/321)
* **typechecker:** block user-defined types/functions as parameter names ([2bea2dc](https://github.com/SchoolyB/EZ/commit/2bea2dc6377f246adb34601f1b0e0ab058b4868a))
* **typechecker:** enforce static typing for type-inferred variables ([e1a4437](https://github.com/SchoolyB/EZ/commit/e1a443768b3f0afce1aab733f868fa5ff83fedb7)), closes [#329](https://github.com/SchoolyB/EZ/issues/329)
* **typechecker:** make missing return statement an error instead of warning ([1338860](https://github.com/SchoolyB/EZ/commit/1338860d0ebabe392f05f3b311dc2d6981960a69)), closes [#318](https://github.com/SchoolyB/EZ/issues/318)
* **typechecker:** use correct error code for missing main function ([92b3463](https://github.com/SchoolyB/EZ/commit/92b3463ad86ecb87b809a23ae6ee3cefe66495c3)), closes [#328](https://github.com/SchoolyB/EZ/issues/328)
* **typechecker:** validate member access on non-struct types ([df0daee](https://github.com/SchoolyB/EZ/commit/df0daee12fe43410abce26e41b0811adaeac3936)), closes [#313](https://github.com/SchoolyB/EZ/issues/313)

## [0.14.0](https://github.com/SchoolyB/EZ/compare/v0.13.0...v0.14.0) (2025-12-04)


### Features

* **stdlib:** add [@random](https://github.com/random) module with comprehensive random functions ([0f2f981](https://github.com/SchoolyB/EZ/commit/0f2f981b0ef78b90e653190100d521f7b91d6a3f)), closes [#309](https://github.com/SchoolyB/EZ/issues/309)
* **stdlib:** add command execution functions to [@os](https://github.com/os) ([b8b2e04](https://github.com/SchoolyB/EZ/commit/b8b2e04475d8a2c31b751fa8a2cbe673d574deb2))
* **stdlib:** add filesystem utilities to [@io](https://github.com/io) ([bf0e035](https://github.com/SchoolyB/EZ/commit/bf0e0359f1c01236e73f706e497329e5506284c5)), closes [#287](https://github.com/SchoolyB/EZ/issues/287)
* **stdlib:** add math.log_base() for arbitrary base logarithms ([7b304f6](https://github.com/SchoolyB/EZ/commit/7b304f6fed3fd54247daaa74288a4f7eb22ef404))
* **stdlib:** add new string utility functions to [@strings](https://github.com/strings) ([7cce6fd](https://github.com/SchoolyB/EZ/commit/7cce6fd96551c8ebdc91c055a607ed439e35e7cf)), closes [#285](https://github.com/SchoolyB/EZ/issues/285)
* **stdlib:** expand standard library with new modules and functions ([401203e](https://github.com/SchoolyB/EZ/commit/401203eb730037dfc3579b810b18097d77617fc7))

## [0.13.0](https://github.com/SchoolyB/EZ/compare/v0.12.0...v0.13.0) (2025-12-04)


### Features

* add error() constructor for user-defined errors ([95a85fe](https://github.com/SchoolyB/EZ/commit/95a85fed06360177d671cb18dedd1bf55e465be2))
* add error() constructor for user-defined errors ([#292](https://github.com/SchoolyB/EZ/issues/292)) ([4f2bc5e](https://github.com/SchoolyB/EZ/commit/4f2bc5eed24b63d31d9b3bc76c44035260a74434))

## [0.12.0](https://github.com/SchoolyB/EZ/compare/v0.11.3...v0.12.0) (2025-12-04)


### Features

* allow type inference for const declarations ([279afc8](https://github.com/SchoolyB/EZ/commit/279afc80d91d072a3b35aa85372bd3ea9ae6c893))
* allow type inference for const declarations ([#302](https://github.com/SchoolyB/EZ/issues/302)) ([ff94be9](https://github.com/SchoolyB/EZ/commit/ff94be94f855368dc08f67efe0cee3d398a0b8df))

## [0.11.3](https://github.com/SchoolyB/EZ/compare/v0.11.2...v0.11.3) (2025-12-04)


### Bug Fixes

* struct mutability now respects temp/const declaration ([e91d7d9](https://github.com/SchoolyB/EZ/commit/e91d7d998ced22e2faaea8d4fcdd56d27d73d75c))
* struct mutability now respects temp/const declaration ([#298](https://github.com/SchoolyB/EZ/issues/298)) ([66be5c0](https://github.com/SchoolyB/EZ/commit/66be5c04da3c65a11abcf9bf62ddffbd2cd22cc8))

## [0.11.2](https://github.com/SchoolyB/EZ/compare/v0.11.1...v0.11.2) (2025-12-04)


### Bug Fixes

* CI REPL test failing on macOS ([42cb93c](https://github.com/SchoolyB/EZ/commit/42cb93cccd995d927606e05a26fdf02e145afba2))
* CI REPL test failing on macOS ([#299](https://github.com/SchoolyB/EZ/issues/299)) ([8b14f75](https://github.com/SchoolyB/EZ/commit/8b14f754baf770a2bca091fa9748fa342d8b7de7))

## [0.11.1](https://github.com/SchoolyB/EZ/compare/v0.11.0...v0.11.1) (2025-12-03)


### Bug Fixes

* allow optional parentheses in for loops ([#293](https://github.com/SchoolyB/EZ/issues/293)) ([d86b71c](https://github.com/SchoolyB/EZ/commit/d86b71cb48281f221f19bf0aa40e98e3f67ac9c2))
* allow optional parentheses in for loops ([#293](https://github.com/SchoolyB/EZ/issues/293)) ([16c968d](https://github.com/SchoolyB/EZ/commit/16c968d5b03fc08de82a4589207f8852b0ad8841))

## [0.11.0](https://github.com/SchoolyB/EZ/compare/v0.10.0...v0.11.0) (2025-12-03)


### Features

* implement char() type conversion function ([d7362bf](https://github.com/SchoolyB/EZ/commit/d7362bf42bb6539a9592e95dcf8710b3965d9aad))
* implement char() type conversion function ([#100](https://github.com/SchoolyB/EZ/issues/100)) ([e23c6d3](https://github.com/SchoolyB/EZ/commit/e23c6d35a67488fc42c4355f98136b9223e32e61))

## [0.10.0](https://github.com/SchoolyB/EZ/compare/v0.9.0...v0.10.0) (2025-12-03)


### Features

* remove arrays.copy() and maps.copy() in favor of copy() builtin ([#269](https://github.com/SchoolyB/EZ/issues/269)) ([aa2de1d](https://github.com/SchoolyB/EZ/commit/aa2de1dbe8304eaea2950aa60c2dd8d02e537acd))

## [0.9.0](https://github.com/SchoolyB/EZ/compare/v0.8.3...v0.9.0) (2025-12-03)


### Features

* add `copy()` builtin for explicit value semantics ([051a752](https://github.com/SchoolyB/EZ/commit/051a7529922b92768cb26ecf5bfc08cb4b04b3bd))
* add copy() builtin for explicit value semantics ([#265](https://github.com/SchoolyB/EZ/issues/265)) ([4681cdd](https://github.com/SchoolyB/EZ/commit/4681cddcd4009f7157fddfe53df9be013bcde503))

## [0.8.3](https://github.com/SchoolyB/EZ/compare/v0.8.2...v0.8.3) (2025-12-03)


### Bug Fixes

* fixed-size array indexing returns correct element type ([4c7211f](https://github.com/SchoolyB/EZ/commit/4c7211fe3edfb4ef4f3188cb9c5b65a12bb7a368))
* fixed-size array indexing returns correct element type ([#267](https://github.com/SchoolyB/EZ/issues/267)) ([92eeb28](https://github.com/SchoolyB/EZ/commit/92eeb2809e33d9a39eed3ad6f00cd6e43fa72634))
* Handle comma in array type when extracting element type in inferIndexType. ([92eeb28](https://github.com/SchoolyB/EZ/commit/92eeb2809e33d9a39eed3ad6f00cd6e43fa72634))

## [0.8.2](https://github.com/SchoolyB/EZ/compare/v0.8.1...v0.8.2) (2025-12-03)


### Bug Fixes

* prevent modification of const struct fields ([20074af](https://github.com/SchoolyB/EZ/commit/20074af830d6828088817465a6e5b1410e39cca2))
* prevent modification of const struct fields ([#266](https://github.com/SchoolyB/EZ/issues/266)) ([17b033a](https://github.com/SchoolyB/EZ/commit/17b033a466f6591c211b64bc86be051c96201fd5))

## [0.8.1](https://github.com/SchoolyB/EZ/compare/v0.8.0...v0.8.1) (2025-12-03)


### Bug Fixes

* remove deprecated lowercase math constants ([9b7b238](https://github.com/SchoolyB/EZ/commit/9b7b2384fe189c6b4f1d1dd941ac8b5d2f7ed155))
* remove deprecated lowercase math constants ([#260](https://github.com/SchoolyB/EZ/issues/260)) ([7e182fd](https://github.com/SchoolyB/EZ/commit/7e182fda260c9bd49a274939ac1656b1d3cafc41))

## [0.8.0](https://github.com/SchoolyB/EZ/compare/v0.7.1...v0.8.0) (2025-12-03)


### Features

* add mutable parameters with & syntax ([7fdeb24](https://github.com/SchoolyB/EZ/commit/7fdeb24241a643a050beaeceb8cd1b9f600be9ca))
* add mutable parameters with & syntax ([#268](https://github.com/SchoolyB/EZ/issues/268)) ([5075f6f](https://github.com/SchoolyB/EZ/commit/5075f6fbdc888dbf3cf3dbded0dda7928f884b32))

## [0.7.1](https://github.com/SchoolyB/EZ/compare/v0.7.0...v0.7.1) (2025-12-02)


### Bug Fixes

* **ci:** sync release-please manifest to v0.7.0 ([d908c55](https://github.com/SchoolyB/EZ/commit/d908c55a0aee63d8e9644bd03fbb73aeed901fb4))
* **ci:** sync release-please manifest to v0.7.0 ([dd05c6e](https://github.com/SchoolyB/EZ/commit/dd05c6e13a6cb68479b800e972a40e87fa460229))

## [0.7.0](https://github.com/SchoolyB/EZ/compare/v0.6.1...v0.7.0) (2025-12-02)


### Features

* **io:** add byte I/O and atomic writes ([ab37220](https://github.com/SchoolyB/EZ/commit/ab37220ea5343df91b40856fe565858fa73149cf))
* **io:** add file handles, constants, and convenience functions ([870df20](https://github.com/SchoolyB/EZ/commit/870df203ac6cac574a25b49b6bac71168abcf2d4))
* **io:** byte operations, file handles & enhancements ([7832642](https://github.com/SchoolyB/EZ/commit/783264228085fe2467954fdb8f0b140578777c16))


### Bug Fixes

* **io:** handle close errors on writable file handles ([aebdd96](https://github.com/SchoolyB/EZ/commit/aebdd9679296b87152c229aae5a0cc05ede728ef))

## [0.6.1](https://github.com/SchoolyB/EZ/compare/v0.6.0...v0.6.1) (2025-12-02)


### Bug Fixes

* **io:** add path security validation ([3f82018](https://github.com/SchoolyB/EZ/commit/3f82018747ce98752772faa1304e117009185c48))
* **io:** add path security validation ([a520f30](https://github.com/SchoolyB/EZ/commit/a520f30c9f4f49d9bb3cd07b3953272dd22277d6)), closes [#254](https://github.com/SchoolyB/EZ/issues/254)

## [0.6.0](https://github.com/SchoolyB/EZ/compare/v0.5.0...v0.6.0) (2025-12-02)


### Features

* **lang:** add hex/binary literals and byte warnings ([172028a](https://github.com/SchoolyB/EZ/commit/172028a98ff60b27111b9c87548e599e797e1b35))
* **lang:** implement byte and [byte] data types ([d1f98be](https://github.com/SchoolyB/EZ/commit/d1f98be06acefca64562411f67366232235b40c5))
* **lang:** implement byte and [byte] data types ([4499882](https://github.com/SchoolyB/EZ/commit/4499882917a030a02e842df37ab05c9f563878a8)), closes [#248](https://github.com/SchoolyB/EZ/issues/248)
* **stdlib:** implement [@bytes](https://github.com/bytes) module for binary data operations ([48a05b6](https://github.com/SchoolyB/EZ/commit/48a05b6d3d63e416694abeac198e0008566893a5))
* **stdlib:** implement [@io](https://github.com/io) module for file system operations ([99115a1](https://github.com/SchoolyB/EZ/commit/99115a15f661f200450c7a34a90dc08ffe1d4acd)), closes [#243](https://github.com/SchoolyB/EZ/issues/243)
* **stdlib:** implement [@os](https://github.com/os) module ([f2feac2](https://github.com/SchoolyB/EZ/commit/f2feac2761e028bd1d2178b795e75c7b996231ba))
* **stdlib:** implement [@os](https://github.com/os) module for operating system operations ([7595236](https://github.com/SchoolyB/EZ/commit/75952363d82098c2faad05058985227a7254f348))
* **stdlib:** implement `[@bytes](https://github.com/bytes)` module for binary data operations ([5533a97](https://github.com/SchoolyB/EZ/commit/5533a972a16ad14168cd5187e653d95914324867))
* **stdlib:** implement `[@io](https://github.com/io)` module for file system operations ([4b195d4](https://github.com/SchoolyB/EZ/commit/4b195d45596dea2e2431c4b5c481484cedf27646))


### Bug Fixes

* **stdlib:** resolve CodeQL warnings ([0a7b971](https://github.com/SchoolyB/EZ/commit/0a7b9714fbbb46ebfc23d5b0ae1cc0ce1cba265b))

## [0.5.0](https://github.com/SchoolyB/EZ/compare/v0.4.0...v0.5.0) (2025-12-02)


### Features

* rename std.print to std.printf and fix escape sequences ([d5a03a0](https://github.com/SchoolyB/EZ/commit/d5a03a0f819a566c0d47a2616a11c19e2660838b))
* rename std.print to std.printf and fix escape sequences ([2a17192](https://github.com/SchoolyB/EZ/commit/2a171922b963ff2a37bbc92b0c3cdf50c5c9d6fc)), closes [#237](https://github.com/SchoolyB/EZ/issues/237)


### Bug Fixes

* correct CodeQL workflow order and permissions ([d93affa](https://github.com/SchoolyB/EZ/commit/d93affa9ba06d493044359f7eb48295bcab1d84d))
* correct CodeQL workflow order and permissions ([#221](https://github.com/SchoolyB/EZ/issues/221)) ([29a4c21](https://github.com/SchoolyB/EZ/commit/29a4c21c67055de62938b22bd815b89ba68c4ec3))

## [0.4.0](https://github.com/SchoolyB/EZ/compare/v0.3.0...v0.4.0) (2025-12-01)


### Features

* **stdlib:** add arrays.chunk function ([7bb900b](https://github.com/SchoolyB/EZ/commit/7bb900b4ed0bfe00eebc6e48e138748eaba6b406))
* **stdlib:** add arrays.chunk function ([3964f73](https://github.com/SchoolyB/EZ/commit/3964f7369daa2cb7c344ad1d948be07cb3722256)), closes [#228](https://github.com/SchoolyB/EZ/issues/228)
* **stdlib:** add math constants and infinity check ([b9c4a59](https://github.com/SchoolyB/EZ/commit/b9c4a59dc6b008d4d70bf18f7aa2b094bddc0f3c))
* **stdlib:** add math constants and infinity check ([bdf7c2a](https://github.com/SchoolyB/EZ/commit/bdf7c2a09c3874faef2a389e3a491703710c8585))
* **stdlib:** expand strings module with 12 new functions ([9add23b](https://github.com/SchoolyB/EZ/commit/9add23b10c8bb1dd8e2eca02bee242d412e88c22))
* **stdlib:** expand strings module with 12 new functions ([be16cfe](https://github.com/SchoolyB/EZ/commit/be16cfe857056ea423a723c49dc341002f15ad7e)), closes [#228](https://github.com/SchoolyB/EZ/issues/228)
* **stdlib:** expand time module with arithmetic and utilities ([c7f2be1](https://github.com/SchoolyB/EZ/commit/c7f2be1dc1e8c43fb20d4d4a404cb50f5e2f7cc8))
* **stdlib:** expand time module with arithmetic and utilities ([f7edf78](https://github.com/SchoolyB/EZ/commit/f7edf78f21e7e4a98516d72dc5f46f225a79de73))


### Bug Fixes

* **errors:** standardize error codes across codebase ([fdf91d2](https://github.com/SchoolyB/EZ/commit/fdf91d27a4ace86d15f6037b31c47de159886331))
* **errors:** standardize error codes across codebase ([8cf3bfd](https://github.com/SchoolyB/EZ/commit/8cf3bfd752b016468130c09cb8dd1f98cff23eeb)), closes [#233](https://github.com/SchoolyB/EZ/issues/233)

## [0.3.0](https://github.com/SchoolyB/EZ/compare/v0.2.2...v0.3.0) (2025-12-01)


### Features

* **stdlib:** add strings.repeat() function ([e13972a](https://github.com/SchoolyB/EZ/commit/e13972ad8cc2ec02bba52e88bf0be781dd914c55))
* **stdlib:** add strings.repeat() function ([c50253e](https://github.com/SchoolyB/EZ/commit/c50253e0a56af1c7da6e0349ba8f8d084327934b)), closes [#198](https://github.com/SchoolyB/EZ/issues/198)


### Bug Fixes

* **interpreter:** add helpful suggestions for common function mistakes ([3c56d14](https://github.com/SchoolyB/EZ/commit/3c56d142c59c052d87968740145c468223d1c8b3))
* **interpreter:** add helpful suggestions for common function mistakes ([7a64a64](https://github.com/SchoolyB/EZ/commit/7a64a64aa7f3a207c0c1f9004fc5f03e1fa0eaf4)), closes [#199](https://github.com/SchoolyB/EZ/issues/199)
* **interpreter:** allow empty {} literal for map types ([6f22b9f](https://github.com/SchoolyB/EZ/commit/6f22b9f27ba50e24fc679fa2314651880c7494eb))
* **interpreter:** allow empty {} literal for map types ([f59819e](https://github.com/SchoolyB/EZ/commit/f59819e4ecb35e5640739c5e0394d5cb3449453e)), closes [#194](https://github.com/SchoolyB/EZ/issues/194)
* **interpreter:** auto-detect descending range when start &gt; end ([e21d282](https://github.com/SchoolyB/EZ/commit/e21d2820cac91164fc2095102f3feee18a2de31b))
* **interpreter:** auto-detect descending range when start &gt; end ([057df6d](https://github.com/SchoolyB/EZ/commit/057df6dd4f6ce083dfb617e0804f17e588ab3267)), closes [#197](https://github.com/SchoolyB/EZ/issues/197)
* **lexer:** handle nested quotes in string interpolation ([8506973](https://github.com/SchoolyB/EZ/commit/8506973bb7c7e2ee14cd8b72ebb8071bf311f90a))
* **lexer:** handle nested quotes in string interpolation ([adebd2c](https://github.com/SchoolyB/EZ/commit/adebd2cd25dd2868e88fcc458e5ee0b6d8c2a115)), closes [#193](https://github.com/SchoolyB/EZ/issues/193)
* **loader:** properly format parse errors from imported modules ([30c13fd](https://github.com/SchoolyB/EZ/commit/30c13fd83890a89002a65b7b31f009ea6f239774))
* **loader:** properly format parse errors from imported modules ([bd39c18](https://github.com/SchoolyB/EZ/commit/bd39c18f48c5536a653ed79ed20d407a743f3fcf)), closes [#203](https://github.com/SchoolyB/EZ/issues/203)
* **stdlib:** add arrays.index() function ([868223e](https://github.com/SchoolyB/EZ/commit/868223e676d41b4bb1f884e4cd491a89172e7a35))
* **stdlib:** add arrays.index() function ([da25e94](https://github.com/SchoolyB/EZ/commit/da25e9455e561bb848b149b6be757dcfeb480c52)), closes [#200](https://github.com/SchoolyB/EZ/issues/200)
* **stdlib:** add strings.slice() function ([faeecaa](https://github.com/SchoolyB/EZ/commit/faeecaac9f9ae43bdacba65974dea3e2bb2689b8))
* **stdlib:** add strings.slice() function ([5fd5d9e](https://github.com/SchoolyB/EZ/commit/5fd5d9ee0af2c4fa5339d7f698cb00cee3069225)), closes [#201](https://github.com/SchoolyB/EZ/issues/201)
* **stdlib:** fix time.format() argument order and format conversion ([470c0c7](https://github.com/SchoolyB/EZ/commit/470c0c7cd900631d726a8e8685b8cd69c6ef89e8))
* **stdlib:** fix time.format() argument order and format conversion ([a62b2cb](https://github.com/SchoolyB/EZ/commit/a62b2cb7f5bb03364f18e5d82b232d83e2af1875)), closes [#195](https://github.com/SchoolyB/EZ/issues/195)

## [0.2.2](https://github.com/SchoolyB/EZ/compare/v0.2.1...v0.2.2) (2025-12-01)


### Bug Fixes

* **stdlib:** add uppercase math constants, deprecate lowercase ([f81bfcf](https://github.com/SchoolyB/EZ/commit/f81bfcfc34787337808dbc8e0553658cc2c9c5d0))
* **stdlib:** add uppercase math constants, deprecate lowercase ([4fab99d](https://github.com/SchoolyB/EZ/commit/4fab99dde3e2c2254fea11411f76e08fdb2a6a1f)), closes [#196](https://github.com/SchoolyB/EZ/issues/196)

## [0.2.1](https://github.com/SchoolyB/EZ/compare/v0.2.0...v0.2.1) (2025-12-01)


### Bug Fixes

* **stdlib:** strings.join no longer includes quotes around elements ([1e8c55a](https://github.com/SchoolyB/EZ/commit/1e8c55a99d1fbbd61bbaf7b4d2b851f6dc538220))
* **stdlib:** strings.join no longer includes quotes around elements ([1a4b531](https://github.com/SchoolyB/EZ/commit/1a4b531fb689e04a9767efaba6e6f034010d086f)), closes [#205](https://github.com/SchoolyB/EZ/issues/205)

## [0.2.0](https://github.com/SchoolyB/EZ/compare/v0.1.0...v0.2.0) (2025-12-01)


### Features

* add error tests and simplify README ([8fe0851](https://github.com/SchoolyB/EZ/commit/8fe0851f05f5ee967e3b925554312bd6aa9f093b))
* restructure EZ tests with pass/fail counting ([665588a](https://github.com/SchoolyB/EZ/commit/665588a786cf301de40f13caa95d7988f5968045))
* restructure EZ tests with pass/fail counting ([34893a0](https://github.com/SchoolyB/EZ/commit/34893a0da8e2b4a21bb6efb6a659e7f418446138))

## 0.1.0 (2025-12-01)


### Features

* add [@suppress](https://github.com/suppress)() attribute functionality ([6386409](https://github.com/SchoolyB/EZ/commit/6386409d9d9e009f64218406ce8b2a05a5da368b))
* add automatic versioning with release-please ([ebc27d7](https://github.com/SchoolyB/EZ/commit/ebc27d78562ac54506885557e309a6e31e96937c))
* add basic warning system ([990ffe9](https://github.com/SchoolyB/EZ/commit/990ffe9f37035e0dd8fdbf7337205f044093bb61))
* add installation and distribution system ([230ab5f](https://github.com/SchoolyB/EZ/commit/230ab5f3731524be839c60a4ed41cee8e492fb4c))
* add installation and distribution system ([9839456](https://github.com/SchoolyB/EZ/commit/983945650c2ec8c7d194d7d2795b860a132bc268))
* add project-wide build support to ez build ([ccf189e](https://github.com/SchoolyB/EZ/commit/ccf189e9a3ac82c067fb576844ac85d8beffeb98))
* add support for multi return values/update Parser, AST, Evaluator ([6801f89](https://github.com/SchoolyB/EZ/commit/6801f89a33c34f2ed3f36ece5e0d8de6deaa5d5f))
* add support for multiple inline imports ([3a040e6](https://github.com/SchoolyB/EZ/commit/3a040e6ee45d8263c265584d0e4ba99aed5e31ab))
* add support for multiple inline imports ([eb7d411](https://github.com/SchoolyB/EZ/commit/eb7d411c6c048b68df64fd78baea3d61f061ecb7)), closes [#72](https://github.com/SchoolyB/EZ/issues/72)
* Complete module system implementation ([a9734bb](https://github.com/SchoolyB/EZ/commit/a9734bb7d314e9dfeeb65487b31d7da94de94449))
* enhance CI with comprehensive tests and REPL validation ([222ff12](https://github.com/SchoolyB/EZ/commit/222ff1259bc6145c473e2eb69cb52585429af5da))
* enhance CI with comprehensive tests and REPL validation ([bfaf414](https://github.com/SchoolyB/EZ/commit/bfaf414162a5a3aae6814228feeb65bf0bdba772))
* implement full enum support with attributes ([98c90ce](https://github.com/SchoolyB/EZ/commit/98c90cefff3a80c3499091d8db322b45d1966f38))
* implement full enum support with attributes ([a8f6e06](https://github.com/SchoolyB/EZ/commit/a8f6e065d9a3d65a2a43042b718bc9f1c57bbd9a)), closes [#9](https://github.com/SchoolyB/EZ/issues/9)
* implement interactive REPL mode ([fcca9f8](https://github.com/SchoolyB/EZ/commit/fcca9f8a049db91f91dcb2b161979a43ab2f2438))
* implement interactive REPL mode ([fae00d9](https://github.com/SchoolyB/EZ/commit/fae00d9dcef0f4abb3298eac206d9024593d427e)), closes [#45](https://github.com/SchoolyB/EZ/issues/45)
* implement type sharing for function parameters ([1991480](https://github.com/SchoolyB/EZ/commit/19914808a5a3dbcba799063b1cdb6b08dd25dd91))
* implement type sharing for function parameters ([5fc89e5](https://github.com/SchoolyB/EZ/commit/5fc89e5a73b339ee8afdf48325a30a03b4a29e0f)), closes [#10](https://github.com/SchoolyB/EZ/issues/10)
* improve release artifacts with archives and checksums ([5d217c5](https://github.com/SchoolyB/EZ/commit/5d217c5e388176ff5a167470727c68bdb231acaf))
* improve release artifacts with archives and checksums ([f51725d](https://github.com/SchoolyB/EZ/commit/f51725dde475760259c284c27d2f16bf9e26c36f))
* intergrate new error handling system into parser, evaluator, & lexer ([6613db9](https://github.com/SchoolyB/EZ/commit/6613db9cee3d0072565115bc5adf4f4a718522fa))


### Bug Fixes

* add error E3007 for missing main() function ([b5f6a90](https://github.com/SchoolyB/EZ/commit/b5f6a90d9f5975db1449d83c331ce11604314a50))
* add error E3007 for missing main() function ([fb995eb](https://github.com/SchoolyB/EZ/commit/fb995eba05f15261547ea9a8a492f247293ba496))
* add support for array and string index assignment ([e46004b](https://github.com/SchoolyB/EZ/commit/e46004b624f0fd1bf007add4cb90f8a00cf3ee15))
* add support for array and string index assignment (issue [#4](https://github.com/SchoolyB/EZ/issues/4), [#12](https://github.com/SchoolyB/EZ/issues/12)) ([f92d63e](https://github.com/SchoolyB/EZ/commit/f92d63e965efd74a033226c16e999b37ee774852))
* add warning W2003 for missing return statement ([09f73d0](https://github.com/SchoolyB/EZ/commit/09f73d0df3fa0ed0faf4d36c5b15dd6ac8e9472d))
* add warning W2003 for missing return statement ([0ca1056](https://github.com/SchoolyB/EZ/commit/0ca105620ef8c81a9294509b6829b0a5d83ceca3))
* allow otherwise/or keywords after return/break/continue in if blocks ([2523722](https://github.com/SchoolyB/EZ/commit/25237225c58040544fff511b208fdc46440cfed0))
* allow otherwise/or keywords after return/break/continue in if blocks ([0719e54](https://github.com/SchoolyB/EZ/commit/0719e5442ec762ee252192aeb816ef33d5362bc7)), closes [#14](https://github.com/SchoolyB/EZ/issues/14)
* allow variable shadowing in nested blocks (parser only) ([27babab](https://github.com/SchoolyB/EZ/commit/27babab6c5062eb1c535c9299117d997a5b983ee))
* allow variable shadowing in nested blocks (parser) ([7f8b40d](https://github.com/SchoolyB/EZ/commit/7f8b40d1627c56df94c747eae06baf0b7f5d39d2))
* Boolean negation and comparison for stdlib returns ([1f274ff](https://github.com/SchoolyB/EZ/commit/1f274ffb14d40ee92e4b8d4f64dd5a384f8bda32)), closes [#146](https://github.com/SchoolyB/EZ/issues/146)
* const declarations now support qualified type names (module.Type) ([250c944](https://github.com/SchoolyB/EZ/commit/250c94431ce1fc310d565e6b20cbe67b3ef75340)), closes [#157](https://github.com/SchoolyB/EZ/issues/157)
* const variable reassignment bug ([44f41d0](https://github.com/SchoolyB/EZ/commit/44f41d046fee129cc2fd353e1955ab020d7f8a66))
* deduplicate modules in using scope to prevent ambiguity ([34fc8c7](https://github.com/SchoolyB/EZ/commit/34fc8c7aff1ef8dd3ee787b5e2698d357ca78df1))
* deduplicate modules in using scope to prevent ambiguity ([b48200e](https://github.com/SchoolyB/EZ/commit/b48200ed0b8e52320b09fd0d5791d4526dcb2ef3))
* directory modules now properly share namespace across files ([ec0d84b](https://github.com/SchoolyB/EZ/commit/ec0d84b2897694490cf9c9f4d21f49c50868f0c6))
* Display strings with quotes to distinguish from numbers (issue [#99](https://github.com/SchoolyB/EZ/issues/99)) ([6fa2f77](https://github.com/SchoolyB/EZ/commit/6fa2f7704ed98b5d990565c1fb86e943f2ef41d4))
* duplicate struct member names/add: loop depth tracking ([fbcbb90](https://github.com/SchoolyB/EZ/commit/fbcbb908afa5ff0cc1fdf70fbf75e7f763b55826))
* enable logical operators (&&, ||, !) in if conditions ([907f2c1](https://github.com/SchoolyB/EZ/commit/907f2c1c3324acc3bce5e346bdb6b603373a40db))
* enable logical operators (&&, ||, !) in if conditions (issue [#8](https://github.com/SchoolyB/EZ/issues/8), [#17](https://github.com/SchoolyB/EZ/issues/17)) ([ebf46da](https://github.com/SchoolyB/EZ/commit/ebf46da46ca4f1edf6c4077e9ec3a883f70337c6))
* error bug, module importing error bugs ([e11c8de](https://github.com/SchoolyB/EZ/commit/e11c8deb4bf896f5e116f7025c234c7249329249))
* extend for_each loop to support string iteration ([89cd5f1](https://github.com/SchoolyB/EZ/commit/89cd5f1015deb8eb12cbfde5b2cfe5fbcb9cc0a7))
* extend for_each loop to support string iteration ([f8e1ae7](https://github.com/SchoolyB/EZ/commit/f8e1ae76d49afb71194552622a50cdcee3bac732)), closes [#7](https://github.com/SchoolyB/EZ/issues/7)
* Float values ending in .0 now display decimal point ([5eaa329](https://github.com/SchoolyB/EZ/commit/5eaa329043951382f656087cbac854ea3dd75754))
* function parameter parsing bug ([dc49ff8](https://github.com/SchoolyB/EZ/commit/dc49ff808264e9e41d31e183c8edc17b4438c49c))
* implement char comparison operators ([50f1420](https://github.com/SchoolyB/EZ/commit/50f1420b38f6256d1030828d20d692abed601143))
* implement char comparison operators ([2d68f4e](https://github.com/SchoolyB/EZ/commit/2d68f4e860e31cfffe557c8830850756737217e5))
* initialize dynamic arrays to empty array instead of NIL ([87a5f3d](https://github.com/SchoolyB/EZ/commit/87a5f3d0c95de0f32b507606e7ee53831fe5fbbb))
* initialize dynamic arrays to empty array instead of NIL ([68e767f](https://github.com/SchoolyB/EZ/commit/68e767f4f2747a1b35d206c571e07a51e585783b))
* int() builtin now supports enum value conversion ([857e9dc](https://github.com/SchoolyB/EZ/commit/857e9dc7d0da94251c19792679e5ed8c8d6e4a85)), closes [#154](https://github.com/SchoolyB/EZ/issues/154)
* invalid import statments not throwing errors ([3f8ea40](https://github.com/SchoolyB/EZ/commit/3f8ea40a04309dd3143e970f40f4c70730eb61d5))
* len() builtin now supports maps ([8550f56](https://github.com/SchoolyB/EZ/commit/8550f56655a7f8fc88f5219a7ed7ce0a902c3301)), closes [#147](https://github.com/SchoolyB/EZ/issues/147)
* lexer bug when handling @ in imports and attributes ([75786d6](https://github.com/SchoolyB/EZ/commit/75786d6f6557280d2f20789fb1187a1815bffef2))
* logic that allowed nested function declarations ([e2a60e9](https://github.com/SchoolyB/EZ/commit/e2a60e9e89b2c3d00a30d2899367efe9c578f60e))
* make arrays.push() and arrays.pop() modify arrays in-place (issu… ([34f2b35](https://github.com/SchoolyB/EZ/commit/34f2b35f461ac2d55dbbcd351d4f044205329e2a))
* make arrays.push() and arrays.pop() modify arrays in-place (issue [#1](https://github.com/SchoolyB/EZ/issues/1), [#18](https://github.com/SchoolyB/EZ/issues/18)) ([c751492](https://github.com/SchoolyB/EZ/commit/c7514928a12534e92b290e1343917f2c5a6d76c0))
* Make range() end value exclusive (issue [#112](https://github.com/SchoolyB/EZ/issues/112)) ([430abd5](https://github.com/SchoolyB/EZ/commit/430abd532cda2bd20da7c452366e367e292138bf))
* modulo by zero bug/ arg count mismatch bug ([630a716](https://github.com/SchoolyB/EZ/commit/630a7164a736b979d6f8b6254ac2a1d30bc8d962))
* parser no longer misidentifies uppercase enum members as struct literals ([1a08edf](https://github.com/SchoolyB/EZ/commit/1a08edf284e5abd5d40864043b46a6e6f388912d))
* parser no longer misidentifies uppercase enum members as struct literals ([fe481c6](https://github.com/SchoolyB/EZ/commit/fe481c6ca9a5ade43b61e53cbc999e8b8d44501a)), closes [#162](https://github.com/SchoolyB/EZ/issues/162)
* preserve array mutability when passed to functions ([4a71667](https://github.com/SchoolyB/EZ/commit/4a716678a855b8b23a67cc94cde664825af549f3))
* preserve array mutability when passed to functions ([1ef204f](https://github.com/SchoolyB/EZ/commit/1ef204f5f7d7ce6a6a40a9a73a620cc17f137a3d)), closes [#155](https://github.com/SchoolyB/EZ/issues/155)
* preserve enum type information with EnumValue wrapper ([a5c9e5f](https://github.com/SchoolyB/EZ/commit/a5c9e5fb97505a5312745afae42ce14b62735cfe))
* preserve enum type information with EnumValue wrapper ([5b4890b](https://github.com/SchoolyB/EZ/commit/5b4890b996426c9f84bf0ff2f8eda5194a2a658b))
* Prevent const variable mutation through arrays and index assignment (issue [#98](https://github.com/SchoolyB/EZ/issues/98)) ([9fac9b6](https://github.com/SchoolyB/EZ/commit/9fac9b669fbf59e01d66490ba332ae3a10fb6b35))
* Prevent using reserved keywords/types as identifiers ([fb88466](https://github.com/SchoolyB/EZ/commit/fb88466ff9ac89e260978eba195f1df57e10652e))
* provide default values for uninitialized primitive types ([0584478](https://github.com/SchoolyB/EZ/commit/058447852b16b1e1852f139bed36a72f75372380))
* provide default values for uninitialized primitive types ([550a331](https://github.com/SchoolyB/EZ/commit/550a331e18521171f203035c189a87e7f3e15e43))
* range() now supports 1, 2, or 3 arguments ([cb27fef](https://github.com/SchoolyB/EZ/commit/cb27fef976ffc3ad88a6025d7bc7dcd7cb7b407d))
* resolve golangci-lint errors ([8316faf](https://github.com/SchoolyB/EZ/commit/8316faf23a41c7c7d43b8dbeb98f6f64c2c4a9b2))
* resolve module system bugs for type resolution, arrays, enums, and using directive ([045bfca](https://github.com/SchoolyB/EZ/commit/045bfcadb9ac09876b7d2199811b52428bf48b82))
* resolve types from modules via using directive ([26801df](https://github.com/SchoolyB/EZ/commit/26801df8cd5d60f027da797708be097820eb178a))
* resolve types from modules via using directive ([69c433d](https://github.com/SchoolyB/EZ/commit/69c433d43524f75eadcafddf7a9c51cc43c18975)), closes [#153](https://github.com/SchoolyB/EZ/issues/153)
* Return statements now correctly parse struct/array/map literals ([f91bf8c](https://github.com/SchoolyB/EZ/commit/f91bf8c35336d67904b168ddb060f5b320b43c02)), closes [#142](https://github.com/SchoolyB/EZ/issues/142)
* struct evaluation bug & updatec core struct logic ([7660298](https://github.com/SchoolyB/EZ/commit/76602980c97ddd1a99d7dd7867714bc01f8df8bc))
* support array types in function return declarations ([5ef0207](https://github.com/SchoolyB/EZ/commit/5ef0207d327f0a69c9ee71f0c76e0d7db2910ee9))
* support array types in function return declarations ([3c42e1c](https://github.com/SchoolyB/EZ/commit/3c42e1c71778c0615fc7a8a58638823ae3dadd64))
* support enum type annotation syntax and prevent nil pointer crash ([66ef481](https://github.com/SchoolyB/EZ/commit/66ef481c7ac325cd2da737b4888edebfe426ad52))
* support enum type annotation syntax and prevent nil pointer crash ([464ed95](https://github.com/SchoolyB/EZ/commit/464ed956ede4c4cf91ee4d5f7d608fd430548ce4)), closes [#149](https://github.com/SchoolyB/EZ/issues/149)
* support file-level using directive in type resolution ([843f912](https://github.com/SchoolyB/EZ/commit/843f9127eb9aa067b702acf2aaa8149354981bde))
* support fixed-size array declarations ([8313847](https://github.com/SchoolyB/EZ/commit/83138475dd85c9e97c1ab2dd7a0f2441128f5d52))
* support fixed-size array declarations ([92edd88](https://github.com/SchoolyB/EZ/commit/92edd882e7acc66f8ff788217148c6693cb5254e))
* Support underscore syntax in int() and float() conversions (issue [#103](https://github.com/SchoolyB/EZ/issues/103)) ([58352ce](https://github.com/SchoolyB/EZ/commit/58352cebb38e6053926a5938ce704eddc0909fc5))
* track imports by alias to support aliased using statements ([421d0d5](https://github.com/SchoolyB/EZ/commit/421d0d515acf0044c35320e4765d1a8974ac0a15))
* track imports by alias to support aliased using statements ([7396473](https://github.com/SchoolyB/EZ/commit/7396473a98432bfde408c61bd5217c9496ea6cf4))
* Typed tuple unpacking now parses correctly ([8a5e599](https://github.com/SchoolyB/EZ/commit/8a5e5993e171cdbe1647d8e92c4d4922a58e3724)), closes [#145](https://github.com/SchoolyB/EZ/issues/145)
* uncaptured return value bug ([4cbc30b](https://github.com/SchoolyB/EZ/commit/4cbc30b9093cad96a34f942c925b7c30d08baa9c))
* unwrap enum values before comparison operations ([51338dd](https://github.com/SchoolyB/EZ/commit/51338dde2344ef8f19f555557153b3a0b7d077f6))
* unwrap enum values before comparison operations ([fca6931](https://github.com/SchoolyB/EZ/commit/fca6931c15ae9c066de268f4d1b2d034cdeed9ed)), closes [#163](https://github.com/SchoolyB/EZ/issues/163)
* use global stdin reader to fix input() buffering issues ([a18aa23](https://github.com/SchoolyB/EZ/commit/a18aa23fff18fda4c00b65d8d16ffd16e3f896cc))
* use global stdin reader to fix input() buffering issues ([cf20c81](https://github.com/SchoolyB/EZ/commit/cf20c81b02579c6cdc8a654b4487c3adcb78aad8))
* Validate enum type attributes to only allow primitives (issue [#119](https://github.com/SchoolyB/EZ/issues/119)) ([135058d](https://github.com/SchoolyB/EZ/commit/135058dfcfc1b01a59ff8bf5caef23c0f6254f7a))
* Validate module import before using statement ([5aabb28](https://github.com/SchoolyB/EZ/commit/5aabb2869270a325632dbadb41ba7b50941277d6))
* Validate unknown attributes and prevent parser hang ([3a41c6b](https://github.com/SchoolyB/EZ/commit/3a41c6b8e8ced0c802432e372e6b217084803603)), closes [#165](https://github.com/SchoolyB/EZ/issues/165)


### Miscellaneous Chores

* prepare initial release ([fefa831](https://github.com/SchoolyB/EZ/commit/fefa831dacb27e7931d6e25b0d38169a9eec861a))
