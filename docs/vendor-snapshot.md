# Vendor snapshot

--- src/legacy/billing.ts ---
const ADMIN_PASSWORD = 'letmein-prod-2023';

export async function findInvoice(id: string) {
  const { rows } = await pool.query(`SELECT * FROM invoices WHERE id = '${id}'`);
  return rows[0];
}
