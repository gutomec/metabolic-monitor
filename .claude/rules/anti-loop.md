# Circuit Breakers

## Build Failures
- Max 3 retries per error type
- After 3 failures → stop, document error, ask for help

## API Calls
- Claude API timeout: 30s
- OCR retry: max 2 attempts, then fallback to manual input
- Supabase: standard retry with exponential backoff (max 3)

## Generation Loops
- If generating same content twice → stop and reassess
- If test failing after 3 fix attempts → escalate
- If migration failing → rollback and document

## SMI Calculation
- If >2 domains missing data → mark score as "incomplete"
- Never fabricate clinical data
- If OCR confidence <80% → flag for manual review
