#UNION TYPE

Which one is active?

`
const std = @import("std");
const print = std.debug.print;

const Payload = union {
    int: i64,
    float: f64,
    boolean: bool,
};

pub fn main() !void {
    atest();
    atest2();
}

fn atest() void {
    const payload = Payload{ .int = 1234 };
    //payload.float = 12.34;
    print("payload {d}\n", .{payload.int});
}

fn atest2() void {
    const payload = Payload{ .float = 124.5 };
    print("playload 2: {d}\n", .{payload.float});
}

`
Labelled unions:

