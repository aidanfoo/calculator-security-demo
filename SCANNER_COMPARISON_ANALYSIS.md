# Scanner Comparison

## Only CodeQL (SAST) Found
- Code patterns and logic errors
- Data flow vulnerabilities
- Unsafe function usage and error-handling issues
- Potential injection paths visible only in source code
- Problems in code branches not triggered during runtime testing 

## Only ZAP (DAST) Found
- Missing security headers
- Runtime configuration issues
- API endpoint vulnerabilities
- Risky server responses (e.g., leaking version info)
- Vulnerabilities triggered only when the app is running
- Input validation issues observable through HTTP interactions

## Only Dependency-Check (SCA) Found
- Outdated package versions
- Known CVEs in dependencies
- Vulnerable versions even if used safely in code\
- Risks introduced through transitive dependencies
- Issues unrelated to logic or runtime behavior but tied to external packages

## All Three Tools
- (Unlikely - they focus on different layers)