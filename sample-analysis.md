ALTER TABLE CUSTOMER ADD COLUMN RISK_LEVEL VARCHAR2(10);

CREATE OR REPLACE VIEW V_CUSTOMER_RISK AS ...

Detected impacts:
- affected views: 3
- affected ETLs: 2
- permission review required
- medium production risk
