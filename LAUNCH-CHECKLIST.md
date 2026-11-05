# MilesHub launch checklist

## Deployment configuration
- [ ] Private Git repository connected to Render
- [ ] PostgreSQL database provisioned and `/api/health` reports connected
- [ ] `SESSION_SECRET` generated securely (32+ characters)
- [ ] Exact HTTPS `APP_ORIGIN` configured without trailing slash
- [ ] Resend sender domain verified; registration and password-reset emails tested
- [ ] First admin created through `npm run create-admin`; credentials stored securely
- [ ] Database backup and restore tested
- [ ] Logs, monitoring, alerting, and incident-response owner configured

## Business and compliance gates — before public transactions
- [ ] Company, tax, privacy, consumer, and payment obligations reviewed by qualified professionals
- [ ] Each airline loyalty programme's current transfer/resale rules reviewed individually
- [ ] Programmes prohibited by their rules or not authorized are disabled
- [ ] Seller identity and evidence reviewed out-of-band before admin verification
- [ ] Seller evidence of control/quantity and permitted transfer method reviewed before listing approval
- [ ] Terms, Privacy Policy, Seller Agreement, refunds/disputes, prohibited-program rules, and support contact published after legal review
- [ ] Payment provider approves the business model; payment integration implemented and tested (not included in current release)
- [ ] Authorized airline fulfilment route documented and tested for each enabled programme (not included in current release)
- [ ] Independent security review / penetration test completed

## Functional testing
- [ ] Customer registration, email verification, login, logout
- [ ] Seller registration, email verification, admin seller verification
- [ ] Unverified sellers cannot publish listings
- [ ] Seller attestation required; unapproved listings remain hidden from customers
- [ ] Admin listing approve/reject and audit log
- [ ] Seller cannot view or edit another seller's listings/orders
- [ ] Order request reserves stock transactionally; concurrent oversell test passed
- [ ] Invalid order status transitions rejected
- [ ] Cancellation restores reserved stock exactly once
- [ ] Password reset link expires and cannot be reused
- [ ] CSRF and cross-origin requests rejected
- [ ] Order summary clearly says it is not proof of payment or miles transfer
- [ ] WhatsApp share link and mobile layout tested

## Never collect
- Airline account passwords, airline OTPs, airline recovery codes
- Raw payment-card numbers or CVVs

## Truthful customer-facing labels
- Seller-entered stock is not a live airline balance.
- Seller attestation is not airline verification.
- An order status is not proof of payment or miles fulfilment.
- Do not advertise any programme as available until its rules and authorized fulfilment path are verified.
