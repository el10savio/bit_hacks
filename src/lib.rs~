pub fn set_kth_bit(x: i32, k: i32) -> i32 {
    x | (1 << k)
}

pub fn clear_kth_bit(x: i32, k: i32) -> i32 {
    x & !(1 << k)
}

pub fn toggle_kth_bit(x: i32, k: i32) -> i32 {
    x ^ (1 << k)
}

pub fn swap(mut x: i32, mut y: i32) -> (i32, i32) {
    x ^= y;
    y ^= x;
    x ^= y;
    (x, y)
}

pub fn min(x: i32, y: i32) -> i32 {
    y ^ ((x ^ y) & if x < y { -1 } else { 0 })
}

#[cfg(test)]
mod tests {
    use super::*;
    #[test]
    fn test_set_kth_bit() {
        assert_eq!(48621, set_kth_bit(48493, 7))
    }
    #[test]
    fn test_clear_kth_bit() {
        assert_eq!(48493, clear_kth_bit(48621, 7))
    }
    #[test]
    fn test_toggle_kth_bit_0_to_1() {
        assert_eq!(48621, toggle_kth_bit(48493, 7))
    }
    #[test]
    fn test_toggle_kth_bit_1_to_0() {
        assert_eq!(48493, toggle_kth_bit(48621, 7))
    }
    #[test]
    fn test_swap() {
        assert_eq!((3, 2), swap(2, 3))
    }
    #[test]
    fn test_min() {
        assert_eq!(2, min(2, 3))
    }
    #[test]
    fn test_min_negative() {
        assert_eq!(-2, min(2, -2))
    }
    #[test]
    fn test_min_same() {
        assert_eq!(2, min(2, 2))
    }
}
